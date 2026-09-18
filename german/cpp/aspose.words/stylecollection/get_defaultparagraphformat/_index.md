---
title: "Aspose::Words::StyleCollection::get_DefaultParagraphFormat Methode"
linktitle: "get_DefaultParagraphFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::StyleCollection::get_DefaultParagraphFormat Methode. Ruft die standardmäßige Absatzformatierung des Dokuments in C++ ab."
type: docs
weight: 7000
url: /de/cpp/aspose.words/stylecollection/get_defaultparagraphformat/
---
## StyleCollection::get_DefaultParagraphFormat method


Ermittelt die standardmäßige Absatzformatierung des Dokuments.

```cpp
System::SharedPtr<Aspose::Words::ParagraphFormat> Aspose::Words::StyleCollection::get_DefaultParagraphFormat()
```

## Hinweise


Beachten Sie, dass dokumentweite Vorgaben in Microsoft Word 2007 eingeführt wurden und nur in OOXML‑Formaten ([Docx](../../loadformat/)) vollständig unterstützt werden. Ältere Dokumentformate unterstützen die standardmäßige Absatzformatierung des Dokuments nicht.

## Beispiele



Zeigt, wie ein [Style](../../style/) zur Stilsammlung eines Dokuments hinzugefügt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// Legen Sie Standardparameter für neue Stile fest, die wir später zu dieser Sammlung hinzufügen können.
styles->get_DefaultFont()->set_Name(u"Courier New");
// Wenn wir einen Stil vom Typ \"StyleType.Paragraph\" hinzufügen, wendet die Sammlung die Werte von
// seiner \"DefaultParagraphFormat\"-Eigenschaft auf die \"ParagraphFormat\"-Eigenschaft des Stils an.
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// Fügen Sie einen Stil hinzu und überprüfen Sie anschließend, ob er die Standardeinstellungen hat.
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## Siehe auch

* Class [ParagraphFormat](../../paragraphformat/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
