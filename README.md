# auto-workflow-scripts

This GitHub repository contains some GitHub automation workflow YAML scripts.

## 0. yaml and github GitHub automation workflow

[introduction](https://docs.github.com/zh/actions)

## 1. usage

```sh
mkdir .github
cd .github
mkdir workflows
```
Then you can add your auto-workflow scripts in .github/workflows.

## 2. settings for sync some files in private to public

### 2.1 Generate PAT

1. Go to [https://github.com/settings/tokens](https://github.com/settings/tokens)

2. Click **"Generate new token (classic)"** under **“Tokens (classic)”**
   (or choose **fine-grained tokens** if preferred)

3. Fill in the token settings:

   * **Note**: e.g. `Push to public repo`
   * **Expiration**: Recommended `90 days` or `No expiration`
   * **Scopes**: Check the following:

     * ✅ `repo` (required for push access)

       * Includes:

         * `repo:status`
         * `repo_deployment`
         * `public_repo`
         * `repo:invite`

4. Click **"Generate token"**
   ✅ **Copy the token** immediately — it will only be shown once!

### 2.2 Add the Token as a Secret in Your Private Repo

1. Open your **private repository**
2. Go to `Settings > Secrets and variables > Actions`
3. Click **"New repository secret"**
4. Fill in:

   * **Name**: `PUBLIC_REPO_TOKEN`
   * **Secret**: Paste the token you just copied
5. Click **"Add secret"** to save


