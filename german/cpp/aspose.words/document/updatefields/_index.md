---
title: "Aspose::Words::Document::UpdateFields Methode"
linktitle: "UpdateFields"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::UpdateFields Methode. Aktualisiert die Werte der Felder im gesamten Dokument in C++."
type: docs
weight: 96000
url: /de/cpp/aspose.words/document/updatefields/
---
## Document::UpdateFields method


Aktualisiert die Werte der Felder im gesamten Dokument.

```cpp
void Aspose::Words::Document::UpdateFields()
```

## Hinweise


Wenn Sie ein Dokument öffnen, ändern und anschließend speichern, aktualisiert Aspose.Words die Felder nicht automatisch, sondern lässt sie unverändert. Daher sollten Sie diese Methode in der Regel vor dem Speichern aufrufen, wenn Sie das Dokument programmgesteuert geändert haben und sicherstellen möchten, dass die korrekten (berechneten) Feldwerte im gespeicherten Dokument erscheinen.

Es ist nicht erforderlich, Felder nach dem Ausführen eines Seriendrucks zu aktualisieren, da der Seriendruck eine Art Feldaktualisierung ist und automatisch alle Felder im Dokument aktualisiert.

Diese Methode aktualisiert nicht alle Feldtypen. Für die detaillierte Liste der unterstützten Feldtypen siehe das Programmierhandbuch.

Diese Methode aktualisiert keine Felder, die mit den Seitenlayout-Algorithmen zusammenhängen (z. B. PAGE, PAGES, PAGEREF). Die seitenlayoutbezogenen Felder werden aktualisiert, wenn Sie ein Dokument rendern oder [UpdatePageLayout](../updatepagelayout/) aufrufen.

Verwenden Sie die Methode [NormalizeFieldTypes](../normalizefieldtypes/), bevor Felder aktualisiert werden, falls Dokumentänderungen die Feldtypen beeinflusst haben.

Um Felder in einem bestimmten Teil des Dokuments zu aktualisieren, verwenden Sie [UpdateFields](../../range/updatefields/).

## Beispiele



Zeigt, wie man ein Inhaltsverzeichnis (TOC) in ein Dokument einfügt, indem man Überschriftenstile als Einträge verwendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügt ein Inhaltsverzeichnis für die erste Seite des Dokuments ein.
// Konfigurieren Sie die Tabelle, um Absätze mit Überschriften der Ebenen 1 bis 3 zu erfassen.
// Stellen Sie außerdem ein, dass seine Einträge Hyperlinks sind, die uns
// zum Ort der Überschrift führen, wenn sie in Microsoft Word mit der linken Maustaste angeklickt werden.
builder->InsertTableOfContents(u"\\o \"1-3\" \\h \\z \\u");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Füllen Sie das Inhaltsverzeichnis, indem Sie Absätze mit Überschriftsformaten hinzufügen.
// Jede solche Überschrift mit einer Ebene zwischen 1 und 3 erzeugt einen Eintrag in der Tabelle.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 2");
builder->Writeln(u"Heading 3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);
builder->Writeln(u"Heading 3.1.1");
builder->Writeln(u"Heading 3.1.2");
builder->Writeln(u"Heading 3.1.3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading4);
builder->Writeln(u"Heading 3.1.3.1");
builder->Writeln(u"Heading 3.1.3.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.2");
builder->Writeln(u"Heading 3.3");

// Ein Inhaltsverzeichnis ist ein Feld eines Typs, das aktualisiert werden muss, um ein aktuelles Ergebnis anzuzeigen.
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertToc.docx");
```


Zeigt die Verwendung des QUOTE-Feldes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügt ein QUOTE-Feld ein, das den Wert seiner Text-Eigenschaft anzeigt.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
field->set_Text(u"\"Quoted text\"");

ASSERT_EQ(u" QUOTE  \"\\\"Quoted text\\\"\"", field->GetFieldCode());

// Fügt ein QUOTE-Feld ein und verschachtelt darin ein DATE-Feld.
// DATE-Felder aktualisieren ihren Wert auf das aktuelle Datum jedes Mal, wenn wir das Dokument mit Microsoft Word öffnen.
// Das Verschachteln des DATE-Feldes innerhalb des QUOTE-Feldes auf diese Weise friert seinen Wert ein.
// auf das Datum, an dem wir das Dokument erstellt haben.
builder->Write(u"\nDocument creation date: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
builder->MoveTo(field->get_Separator());
builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true);

ASSERT_EQ(System::String(u" QUOTE \u0013 DATE \u0014") + System::DateTime::get_Now().get_Date().ToShortDateString() + u"\u0015", field->GetFieldCode());

// Aktualisieren Sie alle Felder, um ihre korrekten Ergebnisse anzuzeigen.
doc->UpdateFields();

ASSERT_EQ(u"\"Quoted text\"", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.QUOTE.docx");
```


Zeigt, wie Benutzerdetails festgelegt und mithilfe von Feldern angezeigt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Erstellen Sie ein UserInformation-Objekt und setzen Sie es als Datenquelle für Felder, die Benutzerinformationen anzeigen.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Name(u"John Doe");
userInformation->set_Initials(u"J. D.");
userInformation->set_Address(u"123 Main Street");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// Fügen Sie die Felder USERNAME, USERINITIALS und USERADDRESS ein, die Werte von
// den jeweiligen Eigenschaften des oben erstellten UserInformation-Objekts.
ASSERT_EQ(userInformation->get_Name(), builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(userInformation->get_Initials(), builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(userInformation->get_Address(), builder->InsertField(u" USERADDRESS ")->get_Result());

// Das Feldoptionen-Objekt verfügt außerdem über einen statischen Standardbenutzer, auf den Felder aus allen Dokumenten verweisen können.
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Name(u"Default User");
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Initials(u"D. U.");
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Address(u"One Microsoft Way");
doc->get_FieldOptions()->set_CurrentUser(Aspose::Words::Fields::UserInformation::get_DefaultUser());

ASSERT_EQ(u"Default User", builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(u"D. U.", builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(u"One Microsoft Way", builder->InsertField(u" USERADDRESS ")->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.CurrentUser.docx");
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
