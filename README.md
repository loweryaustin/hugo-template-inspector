# Hugo Template Inspector

The Hugo Template Inspector is a helper template that prints all template variables in a modal.

![Hugo Template Inspector Version](https://img.shields.io/badge/Version-0.15.2--alpha-brightgreen)

![Release Date](https://img.shields.io/badge/Release%20Date-Mon%2024%20Feb%202020-brightgreen)

![Next Release Date](https://img.shields.io/badge/Next%20Release-Mon%2002%20Mar%202020-brightgreen)


![GitHub issues by-label](https://img.shields.io/github/issues-raw/loweryaustin/hugo-template-inspector/Defect?color=red&label=Open%20Defects)

![GitHub issues by-label](https://img.shields.io/github/issues-raw/loweryaustin/hugo-template-inspector/enhancement?color=green&label=Open%20Feature%20Requests)

## Warning

You should **NOT** use this utility on a site that is acessible to the public. This utility prints a lot of data about your site and server. Some of which could pose security risks if the data were accessible to nefarious individuals (about half of the internet).

### Aww, but Austin, I really want to use this on my publically acessible site!

ಠ_ಠ

## Target Audience

This utility is intended to be used by developers who are creating or modifying Hugo templates.

## Requirements

HTI was built while using Hugo `v0.64.1`. Compatibility with other versions is not currently known.

## Usage

Copy the `inspector.html` into your partials directory. The partials directory can be located under the layouts directory either under the main site root, or within your theme. The following is where this file lives on my particular installation. Your exact loction will likely be different:
```
/Users/username/Sites/websitedir/themes/mycustomtheme/layouts/partials/inspector.html
```

Once the inspector.html file is in place, you'll need to paste the following somewhere in your `baseof.html` template:
```
{{- partial "inspector.html" . -}}
```

I usually put that directly under the opening `<body>` tag.

On a Linux or Mac system, you can find your `baseof.html` template with the following command:
```
find ~ -name baseof.html 2> /dev/null
```

With that file installed, start your Hugo server with the following command:
```
hugo server -D
```

Then browse to your site at:
```
http://localhost:1313
```

And finally activate the modal by pressing the `q` key.

To hide the modal, press the `q` key again.

## Screenshot
