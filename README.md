
You need [Node.js](https://nodejs.org/en/) and npm to be able to build the site.

To install gitbook:

```bash
npm install gitbook-cli -g
```

Install flow plugin:
```bash
npm install gitbook-plugin-flow
```

Install gitbook plugins:

```bash
gitbook install
```

Install gulp and other modules:

```bash
npm install gulp -g
npm install
```

## Preview

To preview the doc, run the following command:

```bash
npm run preview
npm run preview -o file1,file2...
```

The first command will build and launch web server to host the site. It will also enable live reload plugin, so your changes to the markdown source file will automatically triggers the rebuild of the docs.

The second command allows you to build the page that you assigned straightly. Please change the file1,file2... to your own file name, then execute preview command. And this command will help you rebuild the .bookignore file which can let you ignore the files that you didn't change when you rebuild the doc.

After generation finished, don't quit server process, run the following command in other terminal context:

```bash
gulp prune-left-bar
```

This will remove unused links from left bar.

## Build

If you just want to build the markdown to html, use this command:

```bash
npm run build
```

You can also build the doc for ebook formats (PDF, ePub, mobi), please following this guide:

https://toolchain.gitbook.com/ebook.html

If you need to publish to the website, you'd better build it on Mac. If use Windows, some redundant .md file will also generated.