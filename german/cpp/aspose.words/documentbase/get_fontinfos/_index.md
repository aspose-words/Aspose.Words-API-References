---
title: "Aspose::Words::DocumentBase::get_FontInfos Methode"
linktitle: "get_FontInfos"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBase::get_FontInfos Methode. Bietet Zugriff auf Eigenschaften der in diesem Dokument verwendeten Schriftarten in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words/documentbase/get_fontinfos/
---
## DocumentBase::get_FontInfos method


Bietet Zugriff auf die Eigenschaften der in diesem Dokument verwendeten Schriftarten.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> Aspose::Words::DocumentBase::get_FontInfos() const
```

## Hinweise


Diese Sammlung von Schriftartdefinitionen wird unverändert aus dem Dokument geladen. [Font](../../font/) Definitionen können in einigen Dokumenten optional, fehlend oder unvollständig sein.

Verlassen Sie sich nicht auf diese Sammlung, um festzustellen, dass eine bestimmte Schriftart im Dokument verwendet wird. Sie sollten diese Sammlung nur nutzen, um Informationen über Schriftarten zu erhalten, die möglicherweise im Dokument verwendet werden.

## Beispiele



Zeigt, wie man die Details der im Dokument vorhandenen Schriften ausgibt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> allFonts = doc->get_FontInfos();

// Gibt alle verwendeten und nicht verwendeten Schriften im Dokument aus.
for (int32_t i = 0; i < allFonts->get_Count(); i++)
{
    std::cout << System::String::Format(u"Font index #{0}", i) << std::endl;
    std::cout << System::String::Format(u"\tName: {0}", allFonts->idx_get(i)->get_Name()) << std::endl;
    std::cout << System::String::Format(u"\tIs {0}a trueType font", (allFonts->idx_get(i)->get_IsTrueType() ? System::String(u"") : System::String(u"not "))) << std::endl;
}
```


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

* Class [FontInfoCollection](../../../aspose.words.fonts/fontinfocollection/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
