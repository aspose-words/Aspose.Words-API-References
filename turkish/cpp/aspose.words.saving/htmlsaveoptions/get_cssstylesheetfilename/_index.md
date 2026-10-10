---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName method"
linktitle: "get_CssStyleSheetFileName"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName method. Bir belge HTML'ye dışa aktarıldığında yazılan Katmanlı Stil Sayfası (CSS) dosyasının yolunu ve adını belirtir. Varsayılan değer C++'da boş bir dizedir."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_cssstylesheetfilename/
---
## HtmlSaveOptions::get_CssStyleSheetFileName method


Bir belge HTML'ye dışa aktarıldığında yazılan Katmanlı [Style](../../../aspose.words/style/) Sheet (CSS) dosyasının yolunu ve adını belirtir. Varsayılan değer boş bir dizedir.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName() const
```

## Açıklamalar


Bu özellik yalnızca bir belge HTML formatında kaydedilirken ve harici CSS stil sayfası [CssStyleSheetType](../get_cssstylesheettype/) kullanılarak istendiğinde etkili olur.

Bu özellik boş ise, CSS dosyası aynı klasöre ve HTML belgesiyle aynı ada sahip olarak, ancak ".css" uzantısıyla kaydedilir.

Bu özellikte yalnızca yol belirtilmiş ancak dosya adı verilmemişse, CSS dosyası belirtilen klasöre kaydedilir ve HTML belgesiyle aynı ada sahip olur, ancak ".css" uzantısıyla.

Bu özellik tarafından belirtilen klasör mevcut değilse, CSS dosyası kaydedilmeden önce otomatik olarak oluşturulur.

Harici CSS dosyasının kaydedileceği klasörü belirtmenin bir başka yolu, [ResourceFolder](../get_resourcefolder/) kullanmaktır.

## Ayrıca Bakınız

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
