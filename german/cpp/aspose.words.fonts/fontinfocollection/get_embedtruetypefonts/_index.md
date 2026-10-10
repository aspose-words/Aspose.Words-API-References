---
title: "Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts Methode"
linktitle: "get_EmbedTrueTypeFonts"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts Methode. Gibt an, ob TrueType-Schriften in ein Dokument eingebettet werden sollen, wenn es gespeichert wird. Der Standardwert für diese Eigenschaft ist in C++ false."
type: docs
weight: 9000
url: /de/cpp/aspose.words.fonts/fontinfocollection/get_embedtruetypefonts/
---
## FontInfoCollection::get_EmbedTrueTypeFonts method


Gibt an, ob TrueType‑Schriftarten beim Speichern eines Dokuments eingebettet werden sollen oder nicht. Der Standardwert für diese Eigenschaft ist **false**.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts() const
```

## Hinweise


Das Einbetten von TrueType-Schriften ermöglicht es anderen, das Dokument mit denselben Schriften zu sehen, die bei der Erstellung verwendet wurden, kann jedoch die Dokumentgröße erheblich vergrößern.

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
