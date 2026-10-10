---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources yöntemi"
linktitle: "get_ExportFontResources"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources yöntemi. Font kaynaklarının HTML, MHTML veya EPUB formatına aktarılıp aktarılmayacağını belirtir. Varsayılan değer C++'da false'tur."
type: docs
weight: 16000
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_exportfontresources/
---
## HtmlSaveOptions::get_ExportFontResources method


Yazı tipi kaynaklarının HTML, MHTML veya EPUB'a dışa aktarılıp aktarılmayacağını belirtir. Varsayılan değer **false**'tur.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources() const
```

## Açıklamalar


Font kaynaklarını dışa aktarmak, belirli bir kullanıcının ortamında mevcut olan fontlardan bağımsız olarak tutarlı belge render'ı sağlar.

Eğer [ExportFontResources](./) **true** olarak ayarlanırsa, ana HTML belgesi her fonta CSS 3 **%@font-face** at-kurallarıyla başvuracak ve fontlar ayrı dosyalar olarak dışa aktarılacaktır. IDPF EPUB veya MHTML formatlarına dışa aktarırken, fontlar diğer yan dosyalarla birlikte ilgili pakete gömülecektir.

Eğer [ExportFontsAsBase64](../get_exportfontsasbase64/) **true** olarak ayarlanırsa, fontlar ayrı dosyalara kaydedilmeyecek. Bunun yerine, Base64 kodlamasıyla **%@font-face** at-kurallarına gömüleceklerdir.

**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not allow web downloading of their fonts in any form. [License](../../../aspose.words/license/) agreements that cover some fonts specifically note that usage via **%@font-face** rules in CSS style sheets is not allowed. [Font](../../../aspose.words/font/) subsetting can also violate license terms.

## Ayrıca Bakınız

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
