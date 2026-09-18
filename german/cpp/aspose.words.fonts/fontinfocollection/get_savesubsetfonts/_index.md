---
title: "Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts Methode"
linktitle: "get_SaveSubsetFonts"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts Methode. Gibt an, ob ein Teil der eingebetteten TrueType-Schriften mit dem Dokument gespeichert werden soll oder nicht. Der Standardwert für diese Eigenschaft ist false. Diese Option funktioniert nur, wenn die Eigenschaft EmbedTrueTypeFonts in C++ auf true gesetzt ist."
type: docs
weight: 10000
url: /de/cpp/aspose.words.fonts/fontinfocollection/get_savesubsetfonts/
---
## FontInfoCollection::get_SaveSubsetFonts method


Gibt an, ob ein Teil der eingebetteten TrueType-Schriften mit dem Dokument gespeichert werden soll oder nicht. Der Standardwert für diese Eigenschaft ist **false**. Diese Option funktioniert nur, wenn die [EmbedTrueTypeFonts](../get_embedtruetypefonts/) Eigenschaft auf **true** gesetzt ist.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts() const
```


## Beispiele



Zeigt, wie ein Dokument mit eingebetteten TrueType‑Schriftarten gespeichert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> fontInfos = doc->get_FontInfos();
fontInfos->set_EmbedTrueTypeFonts(embedAllFonts);
fontInfos->set_EmbedSystemFonts(embedAllFonts);
fontInfos->set_SaveSubsetFonts(embedAllFonts);

doc->Save(get_ArtifactsDir() + u"Font.FontInfoCollection.docx");
```

## Siehe auch

* Class [FontInfoCollection](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
