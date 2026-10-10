---
title: "Aspose::Words::Layout::PageLayoutCallbackArgs class"
linktitle: "PageLayoutCallbackArgs"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Layout::PageLayoutCallbackArgs class. Ein Argument, das an Notify() übergeben wird. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.layout/pagelayoutcallbackargs/
---
## PageLayoutCallbackArgs class


Ein Argument, das an [Notify()](../ipagelayoutcallback/notify/) übergeben wird. Weitere Informationen finden Sie im Dokumentationsartikel [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/).

```cpp
class PageLayoutCallbackArgs : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Document](./get_document/)() const | Liefert das Dokument. |
| [get_Event](./get_event/)() const | Liefert das Ereignis. |
| [get_PageIndex](./get_pageindex/)() | Liefert den nullbasierten Index der Seite im Dokument, auf die sich dieses Ereignis bezieht. Gibt einen negativen Wert zurück, wenn keine zugehörige Seite vorhanden ist oder die Seite während des Reflows entfernt wurde. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
