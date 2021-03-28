# Webcomic Site Template (Instructions still on going)

## What is it?

A free webcomic template, with instructions on how to set it up (yes, you will have to touch some code, but I'm going to try and make this easy for you).

Built using the static site generator, [Eleventy](https://www.11ty.io/) and using [Netlify CMS](https://www.netlifycms.org/) for the web interface to upload. Hosted on [Netlify], making this site mostly free to maintain except for a domain.

Use it as a starter for your own webcomic.

Based on the [Eleventy Base Blog](https://github.com/11ty/eleventy-base-blog) repo.

## [Demo Site](https://keen-newton-74c4ac.netlify.app/)

## Instructions

### Github account
First thing's first. You're going to need a [Github account](https://github.com/). Github is a bit of a complicated thing to explain, but [here's an article if you want to delve into it](https://www.howtogeek.com/180167/htg-explains-what-is-github-and-what-do-geeks-use-it-for/). For **our purposes** Github is the place where we will be storing the code and files that will make up your webcomic site, and what we'll use to do some necessary edits for it in the beginning.

Github uses something called version control, which means as you make changes a history of older versions of the site is maintained. SO, if you feel like you've horribly messed up something, there's a way to hit that CTRL Z/undo button, so to speak.

Anyways, go create your account and then come back here.

### Deploy the site!

Hit this button:

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/katedee/eleventy-netlify-webcomic&stack=cms)

Clicking the button above will deploy a copy of the demo website to your Netlify
account (you will also create an account during this process)
and everything needed for running the site.

### Setup authentication

After deploying this project, Netlify Identity will add you as a CMS user and
will email you an invite. It is not necessary to accept this invite if you wish
to use an
[OAuth provider](https://www.netlify.com/docs/identity/#external-provider-login)
(e.g. Github) to manage authentication for your CMS.
It is recommended to use this method of authentication as it removes the need
for an email & password to log in to the CMS and is generally more secure. You
will need to add an OAuth provider in your Netlify app settings under
"Settings" > "Identity" > "External providers".

Once you've added an OAuth provider, navigate to `/admin` on your site, select your provider from the
list, and you should then be logged into your CMS. Cool huh?

Now you're all set, and you can start editing content!

## Gotchas

If you change the repo that was created at deploy time from public to private, you'll need to regenerate your token,
as the token generated using the deploy to Netlify button can only access public repositories. To
regenerate your token, head to "Settings" in your Netlify site dashboard, go to the "Identity"
section, then scroll to "Services" where you'll see an "Edit settings" button. Click that and you'll
see a text link to "Generate access token in GitHub".

If you need any help with setting up Netlify CMS, you can reach out to the Netlify team in the [Netlify CMS Gitter](https://gitter.im/netlify/netlifycms).

## Local development

### 1. Clone this repository:

```
git clone https://github.com/danurbanowicz/eleventy-netlify-boilerplate.git my-blog-name
```


### 2. Navigate to the directory

```
cd my-blog-name
```

Specifically have a look at `.eleventy.js` to see if you want to configure any Eleventy options differently.

### 3. Install dependencies locally

```
npm install @11ty/eleventy
```

### 4. Edit _data/metadata.json

This file contains your site title and author details, and can be used to store any other commonly used site data.

### 5. Run Eleventy (builds the site)

```
npx @11ty/eleventy
```

Or build automatically when a template changes:
```
npx @11ty/eleventy --watch
```

Or in debug mode:
```
DEBUG=* npx @11ty/eleventy
```

## Bug reports, feature requests, etc

This is an ongoing project and I welcome contributions and suggestions! Feel free to submit a PR.

If you need any help with setting up Netlify CMS, you can reach out to the Netlify team in the [Netlify CMS Gitter](https://gitter.im/netlify/netlifycms).
