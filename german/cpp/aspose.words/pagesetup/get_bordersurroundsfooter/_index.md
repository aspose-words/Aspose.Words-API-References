---
title: "Aspose::Words::PageSetup::get_BorderSurroundsFooter Methode"
linktitle: "get_BorderSurroundsFooter"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PageSetup::get_BorderSurroundsFooter-Methode. Gibt an, ob der Seitenrand die Fußzeile ein- oder ausschließt in C++."
type: docs
weight: 8000
url: /de/cpp/aspose.words/pagesetup/get_bordersurroundsfooter/
---
## PageSetup::get_BorderSurroundsFooter method


Gibt an, ob der Seitenrand die Fußzeile ein- oder ausschließt.

```cpp
bool Aspose::Words::PageSetup::get_BorderSurroundsFooter()
```


## Beispiele



Zeigt, wie ein Rand auf die Seite und Kopf-/Fußzeile angewendet wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world! This is the main body text.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"This is the header.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"This is the footer.");
builder->MoveToDocumentEnd();

// Fügen Sie einen blauen Doppelrahmen ein.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Double);
pageSetup->get_Borders()->set_Color(System::Drawing::Color::get_Blue());

// Das PageSetup-Objekt eines Abschnitts verfügt über die Flags "BorderSurroundsHeader" und "BorderSurroundsFooter", die bestimmen
// ob ein Seitenrand den Haupttext umschließt, bzw. ob er die Kopfzeile oder Fußzeile einschließt.
// Setzen Sie das Flag "BorderSurroundsHeader" auf "true", um die Kopfzeile mit unserem Rand zu umschließen,
// und setzen Sie anschließend das Flag "BorderSurroundsFooter", um die Fußzeile außerhalb des Randes zu belassen.
pageSetup->set_BorderSurroundsHeader(true);
pageSetup->set_BorderSurroundsFooter(false);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageBorder.docx");
```

## Siehe auch

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
