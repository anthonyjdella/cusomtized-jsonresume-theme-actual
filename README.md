# Customized JSON Resume Theme: Actual

🖼️ This is a tweaked version of the [Actual theme](https://github.com/davcd/jsonresume-theme-actual). Tweaked to fit my design preferences. Published on NPM and GitHub Registry.

## Notable Changes

* 2 Page version in PDF/printable mode 
* Added sections for speaking and articles
* Style changes

## Prerequisites

To build and start the local server, it needs to use the cli command, which is custom cli I tweaked.

`npm i @anthonyjdella/customized-resume-cli`

## How to Start

`npm run start`

## How to Change

* `assets/pug/template.pug` is the order of the resume.
* `assets/pug/` are the html files for each section
* `assets/styles/style.css` is the styling
* To make changes to the PDF/printable version, make changes in the `@print` section of `assets/styles/style.css`
* Change version number in `package.json`
* Deploy the changes via `npm publish --access public`
* To see changes from `resume.anthonydellavecchia.com` you need to go to the [registry project](https://github.com/anthonyjdella/customized-registry-functions), then cd into `functions`, run `npm i` and `npm update`, then `firebase deploy`.

<details>
  <summary>Click to expand README.md of the source repository!</summary>

# Actual theme for JSON Resume

Minimalist and modern theme for [JSON Resume](https://jsonresume.org/) standard, designed for
the [v1.0.0 version](https://raw.githubusercontent.com/jsonresume/resume-schema/v1.0.0/schema.json).

### Export examples
- [Extended version](docs/resume_extended.pdf)
- [Simple version](docs/resume_simple.pdf)

Maybe you would like to take a look at [jsonresume-theme-actual-letter](https://github.com/davcd/jsonresume-theme-actual-letter) to create your letter.
## Table of contents

- [What is JSON Resume?](#what-is-json-resume)
- [Prerequisites](#prerequisites)
- [Export resume](#export-resume)
- [Contribute](#contribute)
- [Support](#support)

## What is JSON Resume?

> JSON Resume is a community driven open source initiative to create JSON-based standard for resumes.

## Prerequisites

- [node.js](https://nodejs.org/en/) runtime with [resume-cli](https://github.com/jsonresume/resume-cli/)

```bash
npm install -g resume-cli
```

## Export resume

- Create your [resume.json](https://jsonresume.org/schema/) file (you can start by editing [this](/resume.json))

```bash
npm install jsonresume-theme-actual

resume export resume.pdf --format pdf --theme actual
resume export resume.html --format html --theme actual
```

## Contribute

```bash
git clone git@github.com:davcd/jsonresume-theme-actual.git
cd jsonresume-theme-actual

npm install

gulp
```

You can live edit any .scss or .pug file

## Support

This theme supports the following JSON paths

### `resume.basics`

```json
{
  "basics": {
    "name": "Richard Hendriks",
    "label": "Software Developer",
    "email": "rhendriks@mail.com",
    "phone": "(912) 555-4321",
    "url": "http://richardh.example.com",
    "summary": "Lorem ipsum...",
    "location": {
      "city": "San Francisco",
      "countryCode": "US",
      "region": "California"
    },
    "profiles": [
      {
        "url": "https://domain.com/rhendricks"
      }
    ]
  }
}
```

- `resume.basics.name` and `resume.basics.label` are required
- `resume.basics.summary` supports markdown

### `resume.work`

```json
{
  "work": [
    {
      "name": "Facebook",
      "location": "California, United States",
      "position": "Software Engineer",
      "url": "http://facebook.com",
      "startDate": "2016-11-17",
      "summary": "Lorem ipsum...",
      "highlights": [
        "Vitae purus faucibus ornare suspendisse",
        "Ut enim blandit volutpat maecenas"
      ]
    }
  ]
}
```

- `resume.work.summary` supports markdown

### `resume.projects`

```json
{
  "projects": {
    "name": "Node.js",
    "description": "Lorem ipsum...",
    "highlights": [
      "Commodo elit at imperdiet dui",
      "Id volutpat lacus laoreet non"
    ],
    "url": "https://nodejs.org/",
    "roles": [
      "contributor",
      "evangelist"
    ]
  }
}
```
- `resume.projects.description` supports markdown

### `resume.skills`

```json
{
  "skills": [
    {
      "name": "Languages",
      "keywords": [
        "Java",
        "Python"
      ]
    }
  ]
}
```

### `resume.education`

```json
{
  "education": [
    {
      "institution": "University of Stanford",
      "url": "https://www.stanford.edu/",
      "area": "Computer Science",
      "studyType": "Master"
    }
  ]
}
```

- `resume.work.area` and `resume.work.studyType` supports markdown

### `resume.certificates`

```json
{
  "certificates": [
    {
      "name": "AWS Certified Solutions Architect",
      "url": "https://www.your-badge.com",
      "issuer": "Amazon Web Services"
    }
  ]
}
```

- `resume.certificates.name` supports markdown

### `resume.awards`

```json
{
  "awards": [
    {
      "title": "Website of the day",
      "awarder": "Awwward",
      "summary": "Lorem ipsum..."
    }
  ]
}
```
- `resume.awards.summary` supports markdown

### `resume.languages`

```json
{
  "languages": [
    {
      "language": "English",
      "fluency": "Native"
    }
  ]
}
```

### `resume.interests`

```json
{
  "interests": [
    {
      "name": "Open Source"
    }
  ]
}
```

#### `resume.references`, `resume.volunteer` and `resume.publications` fields are not supported yet.
</details>
