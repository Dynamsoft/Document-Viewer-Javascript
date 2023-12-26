# Dynamsoft Document Viewer

![version](https://img.shields.io/npm/v/dynamsoft-document-viewer.svg)
![downloads](https://img.shields.io/npm/dm/dynamsoft-document-viewersvg) 
![jsdelivr](https://img.shields.io/jsdelivr/npm/hm/dynamsoft-document-viewer.svg)
![](https://img.shields.io/snyk/vulnerabilities/npm/dynamsoft-document-viewer.svg)

[Dynamsoft Document Viewer (DDV)](https://www.dynamsoft.com/document-viewer/docs/introduction/index.html) is a versatile SDK designed to offer a range of viewers for configuring and executing various document processing workflows.

Key features include:

- Data Management: Organize, retrieve, and manage documents and pages efficiently.

- Viewer Types: Customize your document interaction with a variety of viewers.

Additionally, DDV enhances functionality by allowing integration with customized image filtering processes and document boundary detection processes. It is particularly recommended to use [Dynamsoft Document Normalizer](https://www.dynamsoft.com/document-normalizer/docs/web/programming/javascript/) for document detection.

DDV enables the seamless creation of a document management web application tailored to your specific workflow, user interface, and style needs.

## Table of Contents

- [System Requirements](#system-requirements)
- [License Key](#license-key)
- [Adding the dependency](#adding-the-dependency)
- [Creating HelloWorld](#creating-helloworld)
- [Documentation](#documentation)
- [Features](#features)
- [Contact Us](#contact-us)
- [License Agreement](#license-agreement)
- [Changelog](#changelog)

# System Requirements

The SDK requires the following features to work:

- `WebAssembly`, `Blob`, `URL`/`createObjectURL`, `Web Workers`

## License Key

[![](https://img.shields.io/badge/Get-30--day%20FREE%20Trial%20License-blue)](https://www.dynamsoft.com/customer/license/trialLicense/?product=ddv&utm_source=npm)

## Adding the dependency

Please refer to [this article](https://www.dynamsoft.com/document-viewer/docs/gettingstarted/add_dependency.html).

## Creating HelloWorld

[How to create HelloWorld](https://www.dynamsoft.com/document-viewer/docs/gettingstarted/helloworld.html)

Review the complete code:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, minimum-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>DDV - HelloWorld</title>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/dynamsoft-document-viewer@latest/dist/ddv.css">
    <script src="https://cdn.jsdelivr.net/npm/dynamsoft-document-viewer@latest/dist/ddv.js"></script>
</head>
<style>
    html,body {
        width: 100%;
        height: 100%;
        margin:0;
        padding:0;
        overscroll-behavior-y: none;
        overflow: hidden;
    }

    #container {
        width: 100%;
        height: 100%;
    }
</style>
<body>
    <div id="container"></div>
</body>
<script type="module">
    (async () => {
        await Dynamsoft.DDV.setConfig({
            license: "your-own-license",
            engineResourcePath: "https://cdn.jsdelivr.net/npm/dynamsoft-document-viewer@latest/dist/engine",
        });
        Dynamsoft.DDV.setProcessingHandler("imageFilter", new Dynamsoft.DDV.ImageFilter());
        const editViewer = new Dynamsoft.DDV.EditViewer({
            container: "container",
        });
    })();
</script>
</html>
```

## Documentation

* [Developer's Guide](https://www.dynamsoft.com/document-viewer/docs/introduction/index.html)
* [API Reference](https://www.dynamsoft.com/document-viewer/docs/api/index.html)

## Features

Generally, the features of DDV can be divided to two parts as below.

### Data Management

Data management is to manage the data which is imported into DDV. It is managed from the following two aspects:

- Document Management: Document creation/deletion/merging, etc.
- Page management: Pages in documents loading/saving/deleting/moving, etc.

### Viewers

Viewers are used to display the data. According to the different uses of viewers, DDV provides five different viewer types, which are implemented through five viewer classes.

- Edit Viewer: Edit the pages in document, such as, rotating, cropping, filtering, etc. and adjust the layout of the display.
- Capture Viewer: Control camera, play video stream, and capture the images from camera.
- Perspective Viewer: Do page boundary manual adjustment & perspective transformation.
- Browse Viewer: Display pages in multiple-mode, pages can be multiple selected.
- Custom Viewer: No built-in UI or functionality, which is used for creating your own viewer.

[More](https://www.dynamsoft.com/document-viewer/docs/features/index.html)

## Contact Us

[Contact Dynamsoft](https://www.dynamsoft.com/company/contact/) to resolve any issue you encounter with the library.

## License Agreement

https://www.dynamsoft.com/company/license-agreement/

## Changelog

Check out the [release notes](https://www.dynamsoft.com/document-viewer/docs/releasenotes/index.html) of the Dynamsoft Document Viewer.
