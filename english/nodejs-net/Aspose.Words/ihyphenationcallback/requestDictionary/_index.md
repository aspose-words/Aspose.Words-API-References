---
title: IHyphenationCallback.requestDictionary method
linktitle: requestDictionary method
articleTitle: requestDictionary method
second_title: Aspose.Words for NodeJs
description: "IHyphenationCallback.requestDictionary method. Notifies application that hyphenation dictionary for the specified language wasn't found and may need to be registered."
type: docs
weight: 10
url: /nodejs-net/Aspose.Words/ihyphenationcallback/requestDictionary/
---

## requestDictionary(language) {#string}

Notifies application that hyphenation dictionary for the specified language wasn't found and may need to be registered.


Implementation should find a dictionary and register it using[Hyphenation.registerDictionary()](../../hyphenation/registerDictionary/#string_buffer) methods.


If dictionary is unavailable for the specified language implementation can opt out of further calls for the same language
using[Hyphenation.registerDictionary()](../../hyphenation/registerDictionary/#string_string) with ``null`` value.



```js
requestDictionary(language: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| language | string | A language name, e.g. "en-US". See .NET documentation for "culture name" and RFC 4646 for details. |

### Remarks

Exceptions thrown by this method will abort execution of page layout process.


### See Also

* module [Aspose.Words](../../)
* class [IHyphenationCallback](../)

