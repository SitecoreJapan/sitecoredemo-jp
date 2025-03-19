# Starter Kit Additional Content

This repository adds sample sites after deploying the Next.js + Tailwind CSS starter kit. Two sample sites are provided.

## Prerequisites

- Deployed XM Cloud instance
- Sitecore CLI

Starter Kit is here.

- https://github.com/SitecoreJapan/tailwind-starter

After deployment, proceed to the next step with one site published.

<img src="images\step1.png" title="Sample Site" alt="Sample Site" />

## Deploying the Site

Use the Sitecore CLI commands to log in to Sitecore XM Cloud and connect to the environment.

```
dotnet sitecore cloud login
dotnet sitecore cloud environment connect -id <Your Environment Key> -aw
```

Next, deploy the sites. In this case, two sites will be deployed.

```
dotnet sitecore ser push -n <instance name> -i doc-sitecoredemo-jp
dotnet sitecore ser push -n <instance name> -i nextjs-starter
```

Once the above steps are completed, two sites will be deployed.

<img src="images\step2.png" title="Additional site" alt="Additional site" />

### sitecoredemo-jp

This site includes the following features:

- Supports Japanese and English languages
- Dark and light mode switching
- Site using Tailwind CSS
- Various components
  - Breadcrumb
  - Code
  - Markdown
  - Google Maps
  - YouTube

A custom Link List has been added. This link list has been modified as follows:

- In editing modes such as Pages, it behaves as usual (using GraphQL for JSON Rendering)
- Outside of editing modes, it only displays published data from GraphQL (fetching data from Experience Edge for rendering)

### nextjs-starter

This site is the Basic Site provided by the Next.js Starter Kit.
