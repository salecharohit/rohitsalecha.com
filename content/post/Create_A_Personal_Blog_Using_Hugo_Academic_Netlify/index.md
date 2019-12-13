---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Create A Personal Blog Using Hugo Academic Netlify"
subtitle: "Create your own personal blog using Hugo Academic and Netlify"
summary: "If you are tired of maintaining a blog on popular blogging websites and looking for a simple and easy to use blogging platform then read on ! "
authors: [rohit]
tags: [blog,hugo,netlify,academic]
categories: [Technology]
date: 2019-12-13T11:12:27+05:30
lastmod: 2019-12-13T11:12:27+05:30
featured: true
draft: false
markup: mmark

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: "Hugo Academic and Netlify"
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

Having a space to express your thoughts or share your knowledge is a soul satisfying endeavour for many. Hence there are multiple blogging platforms like Blogger,Wordpress etc… where we can easily create a website and start writing. I previously used Wordpress(hosted) and Blogger but eventually moved to having a platform which is more flexible to my needs and requirements.

#### Issues with hosted Wordpress solution
If you are using wordpress hosted solution you need to constantly update your plugins and your wordpress core from time to time

Another big problem is of managing TLS certificates. Renewal , payments and configuration everything has to be done manually and to be honest just for a simple blog it was an overkill.

#### Issues with Blogger

Blogger was definitely a notch better than wordpress as i did not have to worry about managing the application and it also provided a TLS certificate with integration with LetsEncrypt. However the customization options and theming options were very much limited.

I tried to customize my blog adding HTML and CSS but then it becomes difficult to manage the content.

#### Hugo,Netlify and Academic

This blog is built using Hugo,Netlify and Academic.

[Hugo](https://gohugo.io/) is a simple framework written in Go which basically converts Markdown files into static HTML and [Academic](https://themes.gohugo.io/academic/) is a templating theme for the same.
[Netlify](https://www.netlify.com/) is a hosting platform where we can deploy our simple markdown files which would then run a build and deploy our website.

The basic advantage of using this approach are

1. We get a simple static website with no overhead of maintenance or updates.
2. Plenty of [themes](https://themes.gohugo.io/) and customization options available.
3. You are simply creating content in Markdown and Hugo+Netlify do all the magic in the backend
4. You get to preview your website locally before pushing changes to production
5. Netlify provides HTTPS service be default for its subdomain as well as any customized domain, provided your NS records point to Netlify more on this later.

So if you are also looking for building a personal blog using Hugo,Academic and Netlify then follow on

#### Accounts Creation

Firstly,you’ll need to create an account with [Netlify https://app.netlify.com/signup](https://app.netlify.com/signup) to host your blog and [Github](https://github.com/),Gitlab or Bitbucket to store your content.
Netlify shall pull the source from your respective repo and build your website using Hugo
Optionally if you would like to have comments on your posts then you can also create an account on Disqus(https://disqus.com/)

#### Installation

Instructions to install Academic and Hugo on Netlify have been detailed here [https://sourcethemes.com/academic/docs/install/](https://sourcethemes.com/academic/docs/install/) 
Sign into your netlify.com and browse to this URL [https://app.netlify.com/start/deploy?repository=https://github.com/sourcethemes/academic-kickstart](https://app.netlify.com/start/deploy?repository=https://github.com/sourcethemes/academic-kickstart) 

As shown below you’ll be prompted for Github access. The permissions here are restricted to only the particular repo that Netlify will create.

![Github Access](https://lh3.googleusercontent.com/jba_eZEoVdUaiwa66Tz4ApXBA6r480bq2maL-T0EAOJLsvHkVwqR8jn275hgyE7e_kcaeQfoi_XDthsChNEaHPExhg6W9DKv_8pmFra6OMp2yxJVHAga9QrvXnLGH-0vCOU8Spnk "Github Access" ) 

After providing the requisite permissions Netlify will ask to create a repository as shown below.
Netlify will basically create and manage a repository on your Github account and pull the changes for building your website. You can give any name to it for ex:  testsite.com

![Create Repo](https://lh4.googleusercontent.com/rxD6msHmVDcwyfWf3tso6O_NKShlceuimFLgWnoMtJ4W7nVFsJggfywihSqjKelpOK16udAaJ0jxkVfOrJW019tugeSR7p0iA7xxmedPHWJzyrroGkNfP3PoYPIgwWG-tF35mkdg)

Click on “Save and Deploy “
This will create a new repository on your Github account filled with all the Hugo and Academic dependencies as shown below.

![Github Repo](https://lh5.googleusercontent.com/Z4Sn-k119vZ-C3vrnRC8k1dLhHuLKJxVzUC6j-usQQ2dWfRbFq2m9DIrAETk60OOrfT6TZRZe1jHv-hDtfp1jLvSm4Wi4Fz3UT8uCdA9TOeP2PLE0BaLxOld47hmgtORafRjBZXR)

Going back to the Netlify console you’ll see that a ''' https://<random-name>.netlify.com ''' website has been generated as shown below.

![Netlify Console](https://lh4.googleusercontent.com/pApU3uh6dx-_Mf9dbMQ00l9GTyWqgfblnFvffJ8k6pXHZWAhMeuKDOBqU6-ykDftjEGw0mg87H-MMlC8uRL9N86iGrsQqKtXzAsFoTQaRcKxPimIcPngv6S32d4pV-_ed4g3Z0Oi)

Lets browse to this new site

![New Site](https://lh4.googleusercontent.com/jjaasLOnvnw7m2NXi1JlMUVk-yHAYE48FuWjDwHWVumUEVutGs235VmZiCAoEGDo5TfXKM8PWHGyuT7nBRi5ts31pnYdDdRqbZep1fO7OVgNyghbqof28DZxzI9x3U5HS0_y_KCU)

> Congratulations ! A brand new Blog with Hugo and Academic is ready !

#### Customizing Your Blog

Next,we are now interested in customizing our website. All we now need to do is move over to our Github repo and simply make the changes ! For Ex: I’ll head over to the [https://github.com/salecharohit/testsite.com/blob/master/content/home/demo.md](https://github.com/salecharohit/testsite.com/blob/master/content/home/demo.md) and delete the demo.md file.

![Customize on Github](https://lh6.googleusercontent.com/57Dk0qIgnCOjODTJHAuaEqNFfS-udRtciwuXiKFfuh9BdfqI_nQ57LCn6GBJcDEzqSdBtV5a0ABsGv8UZtsvthFS6r-aTYnLBZ2Ycx25mmjXYqzX6M7gLdeWIwhzcLp9Ee8QG7uQ)

The moment you delete the file and commit the changes it can be seen that there is a new change being pushed in Netlify’s console.

![Change Published](https://lh3.googleusercontent.com/BM2huU1zzxi-uu9h0VUYf-ZPnFugT29lk_TJeZC5Yaf1apstki3smj-ejhui7hL7BGu7CO9acj15zOEtf9oajGCIQNAgxUxPC5tqJY_ws2A9RTEVIx9njjFGnC7D0URCd8un46aY)

Netlify shall now build and publish our changes on the public site !

However,here we are making changes on github.com which will not be quite desirable to many.
How about making changes locally ? Follow the below steps !

1. Install Git (https://git-scm.com/downloads) if you don't have it already
2. Download the latest Hugo (Extended) binaries from the [releases page](https://github.com/gohugoio/hugo/releases) 
![Releases Page Hugo Extended](https://lh4.googleusercontent.com/xnVpEBTVlurBsZ6zLWRiKMt6kW-LTcviDTI-LhS704dz_ZVUoByL3wfncovmAm-hueIgJwVAiiUp0yvrLB0uPsEs1DRZ15Z6N7z3i_QqoR7qaTRWidyvwXgRKXBUDy7iMEwMRyTe)

3. Clone your testsite.com repo into your local computer
```bash
git clone https://github.com/salecharohit/testsite.com
```
4. Initialize the theme
```bash
cd testsite.com
git submodule update --init --recursive
```
5. Make your changes and then
```bash
git add .
git commit -m “commit message”
git push
```
{{% alert warning %}}
You’ll need to add your Github keys/Credentials in order for git push to work.
{{% /alert %}}

> Awesome ! You are all set to make changes to your own Blog !

#### Understanding the Hugo+Academic Environment

Before we start with anything open a terminal and cd into your repo folder and fire the view.sh script
![view.sh hugo](https://lh4.googleusercontent.com/NHfy5sLFnBC2GFclCMlWDFy2qOihUJ50gPALmHbu4FgJSnvZJFGYEtj5sVCwIRwBBJjKatc7lnIyJ8rcyL1BVtvnnfOzEVNpRZh0dAq1H9Y_QAc22wCCE9G9YZMwagZeD0NTJAR6)

Your website can now be locally previewed on [http://localhost:1313](http://localhost:1313). Keep this running and start editing the website. Hugo will refresh and rebuild the entire website for all the saved changes.

Load your git repository into your favorite Editor. I am using [Visual Studio Code](https://code.visualstudio.com/).

![Load Git Repo](https://lh5.googleusercontent.com/P-l50RLXhjGt7DImNBCRURpWpbcaCahGSbDxsNP9pya1A-AF99MAVibOgTeOdprvwGcZrrCs0DbXnodc8CSZZJ33a8YrOa_jr1ujIYvdBTqT1QgVFum74Cs3ynYVdXOhS5r2e1Y6)

At first glance all the code and folders and config files might look extremely overwhelming but the good news is that we only need to work on two folders viz. .confg and content

![Config and Content Folder](https://lh6.googleusercontent.com/9Ap6CQU5bEG0-cGF1rTBMyyrCBAFoQShkre2H8JpsMJeDjFN10NbgvBcpSjWh6UbD-2KU5neyfI7a5sFBBhQhtZFwSDqrCZjv6AJxv28Z2r8fLrDvSUWMiI5NyCKo_M3wOV6qUII)

The .config folder contains all the configuration options for Hugo and Academic and most options are quite self-explanatory.

The content folder contains all the content that you wish to publish.
The first thing you might want to edit is the author name i.e. your name rather than admin.

To do that first you need to open the [https://github.com/salecharohit/testsite.com/blob/master/content/home/about.md ](https://github.com/salecharohit/testsite.com/blob/master/content/home/about.md) file and edit the highlighted element.Lets say author=test

![Home](https://lh6.googleusercontent.com/lIubRg_-7a2JRqERHrBEK9ndV3uHg7b6Y_iii5mAAfKqZYsXCLRx6OMUPA7A2nkVPTK4dQBOHwC2PaJvYcbwfzUMqtrs1UMO5V5XxhL_bUbznf-DN6Xn12avshdDNhqT5B0Yjp9p)

Next , under the authors folder rename the “admin” folder to whatever name you’ve chosen i.e. test
![rename admin folder](https://lh4.googleusercontent.com/kgrDAD5Xx76F4gvsYTuePUb1X-iSrNnQCACrGxFr21YEmukl5V1Oovpbg47fINIY05ThBjRhL6nkXo1drCyadhRWk6vNilpbD6zXSH_K3ul8ocPmZLRXmi5zbtuhDzxHVPWK1lUA)

Next you may want to modify the _index.md file to reflect your own data.
![Modiy _index.md](https://lh5.googleusercontent.com/NIdqApvrSS-ehnZLw39rBizLGTRpZ6h_p9G7Ezpsh0DQuLXP1hI-kSb09azZoAqzxLQtaI1fTXAOwjdmzOKEt-2KAMHKWy4pB9TP1dC17yi1eNEhB77rwr0tQsfNEk-353ebZFTJ)

Save the changes and then preview your site locally !
![Preview Changes](https://lh4.googleusercontent.com/wKaZQS2MFuuS_3Z5uabzqctwodRlbGsgxMOJpOfnMoC1tv72eR6w4D2rPlmZOD44IkbhafSPs28PHuysZuErsqKCh5D9EV46bna0ZLoNlMBgLWzVHKA6iB5h0zKxzIJaB0LElhQb)

In order to create a new post just fire the command
```bash
hugo new --kind post post/<post_name>
hugo new --kind post post/test_post
```

It’ll create a new folder with the same name as the post name and an _index.md file as shown below.
![New Post](https://lh3.googleusercontent.com/geddXzlW9M6MGG4YC3h10egjU9odJ6AWy_MV-Gu3TxIPSKVyXTcSN22xUI-9RCinyiZCUJIwEbVtgKY3EykGiWceS26eUpEq5wAmGVH5zIbeLyorIa2cbsLImd4hh4ProcIbRgCl)

Now simply add your content in the Markdown format [https://learn.netlify.com/en/cont/markdown/](https://learn.netlify.com/en/cont/markdown/)

![Post in Markdown](https://lh4.googleusercontent.com/V5dhm7OIyiuwSYg0HQkM2eTGyOQu1UF1WJR9Z0rHyBXUBlIt5WmzhqOB8IzulB7L96GUeOuPMIuNZ-Dz4OsvTgxiaVlmzjC5BTSc-KnouRpYPCJJanT545ssODhEerJ5yenox6IQ)

View the changes

![View Changes](https://lh5.googleusercontent.com/AuerzQl0rK1VDxTLBg1CyCRafxvlx5MO7Sq_A2egKUhzU7JbpMzF13BgvnYHtOYYdJcJIjf2b7l8H9v5EvSQZMEiMyxW4x_nvWw8cpC1-dXntEOxSVVx1HZql4834QdXQb1kkOVV)

Academic has many options to take your blog to the next level using [Markdown,Latex and many inbuilt shortcodes](https://sourcethemes.com/academic/docs/writing-markdown-latex/).Your imagination is the limit !

#### Customizing Domain

Using Netlify you can customize the domain name by clicking on “Overview” → “Site Settings” → “Site Details” and “Edit Site Name” as shown below.

![Change Site Name](https://lh6.googleusercontent.com/0hxDnWZTlmEVCcD-ARFvwDaZ00-JWWGP-7AIIWR_fhh5akGqdBemuKgokLXcUsccErZJ0nIS6y8Y5oEQT1pxpQimluiPdXDBMEwRJ8_AvvPBST-d6aZfdtNysU4LmZlyPq7-_lIT)

This will however always give you a sub-domain of netlify.com for example https://testsite.netlify.com

You can also add a custom domain by following the simple steps highlighted in the netlify’s console panel “Overview” → “Domain Settings”.However for that you’ll need to point your DNS Name servers to that of netlify i.e.

```bash
dns1.p07.nsone.net
dns2.p07.nsone.net
dns3.p07.nsone.net
dns4.p07.nsone.net
```
{{% alert warning %}}
NOTE : Before doing this please ensure you take a backup of your DNS Zone records from the earlier NS provider.
{{% /alert %}}

> We have completed the most basic steps to start and run our own blog using Hugo,Netlify and Academic.Hope that helps you to create your own blog which is simple to maintain and easy to configure.