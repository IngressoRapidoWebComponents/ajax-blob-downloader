[![bower version](https://img.shields.io/bower/v/ajax-blob-downloader.svg)](https://libraries.io/bower/ajax-blob-downloader)
[![open issues](https://img.shields.io/github/issues/IngressoRapidoWebComponents%2Fajax-blob-downloader.svg)](https://github.com/IngressoRapidoWebComponents/ajax-blob-downloader/issues)
[![license](https://img.shields.io/github/license/IngressoRapidoWebComponents%2Fajax-blob-downloader.svg)](https://github.com/IngressoRapidoWebComponents/ajax-blob-downloader/blob/master/LICENSE)


# \<ajax-blob-downloader\>

Download blob from ajax request.

_[Demo and API docs](https://ingressorapidowebcomponents.github.io/components/ajax-blob-downloader/)_

### 1) Add the downloader element.

```html
<ajax-blob-downloader
  id="downloader"
  default-file-name="checklist.txt">
</ajax-blob-downloader>`
```

### 2) Add the ajax element that request and receive the blob content.

```html
<iron-ajax
  id="downloadAjax"
  handle-as="blob"
  loading="{{_downloading}}"
  on-response="_onFileDownloaded"
  on-error="_onFileFailed">
</iron-ajax>
```

### 3) Send it to ajax-blob-downloader element from download method.

```js
  _onFileDownloaded(e) {
    this.$.downloader.download(e.detail);
  }
```

### 4) Open the file! :)