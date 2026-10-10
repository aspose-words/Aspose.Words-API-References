---
title: "Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts Methode"
linktitle: "get_EmbedSystemFonts"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts Methode. Gibt an, ob Systemschriftarten in das Dokument eingebettet werden sollen oder nicht. Der Standardwert für diese Eigenschaft ist false. Diese Option funktioniert nur, wenn die EmbedTrueTypeFonts-Option in C++ auf true gesetzt ist."
type: docs
weight: 8000
url: /de/cpp/aspose.words.fonts/fontinfocollection/get_embedsystemfonts/
---
## FontInfoCollection::get_EmbedSystemFonts method


Gibt an, ob Systemschriftarten in das Dokument eingebettet werden sollen oder nicht. Der Standardwert für diese Eigenschaft ist **false**. Diese Option funktioniert nur, wenn die [EmbedTrueTypeFonts](../get_embedtruetypefonts/) Option auf **true** gesetzt ist.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts() const
```

## Hinweise


Das Setzen dieser Eigenschaft auf **true** ist nützlich, wenn der Benutzer ein ostasiatisches System verwendet und ein Dokument erstellen möchte, das von anderen gelesen werden kann, die keine Schriftarten für diese Sprache auf ihrem System haben. Zum Beispiel könnte ein Benutzer eines japanischen Systems wählen, die Schriftarten in ein Dokument einzubetten, sodass das japanische Dokument auf allen Systemen lesbar ist.

Diese Option funktioniert nur für die Formate DOC, DOCX und RTF.

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
