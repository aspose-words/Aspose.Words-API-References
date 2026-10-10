---
title: "Aspose::Words::HeaderFooter::get_IsHeader Methode"
linktitle: "get_IsHeader"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::HeaderFooter::get_IsHeader Methode. Wahr, wenn dieses HeaderFooter-Objekt in C++ eine Kopfzeile ist."
type: docs
weight: 5000
url: /de/cpp/aspose.words/headerfooter/get_isheader/
---
## HeaderFooter::get_IsHeader method


Wahr, wenn dieses [HeaderFooter](../)-Objekt eine Kopfzeile ist.

```cpp
bool Aspose::Words::HeaderFooter::get_IsHeader()
```


## Beispiele



Zeigt, wie man eine Kopfzeile und eine Fußzeile erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Erstelle eine Kopfzeile und füge einen Absatz hinzu. Der Text in diesem Absatz
// wird oben auf jeder Seite dieses Abschnitts angezeigt, über dem Haupttext.
auto header = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(header);

System::SharedPtr<Aspose::Words::Paragraph> para = header->AppendParagraph(u"My header.");

ASSERT_TRUE(header->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

// Erstelle eine Fußzeile und füge einen Absatz hinzu. Der Text in diesem Absatz
// wird unten auf jeder Seite dieses Abschnitts angezeigt, unter dem Haupttext.
auto footer = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(footer);

para = footer->AppendParagraph(u"My footer.");

ASSERT_FALSE(footer->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

ASPOSE_ASSERT_EQ(footer, para->get_ParentStory());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), para->get_ParentSection());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), header->get_ParentSection());

doc->Save(get_ArtifactsDir() + u"HeaderFooter.Create.docx");
```

## Siehe auch

* Class [HeaderFooter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
