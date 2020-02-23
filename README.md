# Hugo Template Inspector

The Hugo Template Inspector is a helper template that prints all template variables in a modal.

**Version:** 0.13.0

## Warning

You should **NOT** use this utility on a site that is acessible to the public. This utility prints a lot of data about your site and server. Some of which could pose security risks if the data were accessible to nefarious individuals (about half of the internet).

### Aww, but Austin, I really want to use this on my publically acessible site!

ಠ_ಠ

## Target Audience

This utility is intended to be used by developers who are creating or modifying Hugo templates.

## Requirements

HTI was built while using Hugo `v0.64.1`. Compatibility with other versions is not currently known.

## Defects, Improvements, etc.

If you find a problem with HTI, or you have a feature request, please create a GitHub issue with the following information:

### For Defect Reports

- Your version of Hugo
- The filesystem path to the inspector.html file.
- The information that proves that the defect is caused by HTI.
- If an error is produced, a copy of the error in both text format and screenshot.
- If undesireable behavior occurs, a description of the undesireble behavior.
- The steps required to reproduce the problem.
- Any related resources you may have found while researching to confirm that the problem is caused by HTI.

### For Improvement/Feature Requests

- A description of the problem that your proposed feature / improvement would solve.
- A description of how your proposed feature would work / or change the current behavior of HTI.
- Any suggestions you might have about how the feature / improvement might be implemented.

The following guidelines are important to consider before making a feature request:

- HTI should remain a single file without external dependancies
- New additions should avoid creating compatibility issues with other software that it HTI would co-exist with.

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
