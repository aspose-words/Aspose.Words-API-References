---
title: "Aspose::Words::DocumentBuilder::InsertHyperlink Methode"
linktitle: "InsertHyperlink"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::InsertHyperlink Methode. Fügt einen Hyperlink in das Dokument in C++ ein."
type: docs
weight: 38000
url: /de/cpp/aspose.words/documentbuilder/inserthyperlink/
---
## DocumentBuilder::InsertHyperlink method


Fügt einen Hyperlink in das Dokument ein.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertHyperlink(const System::String &displayText, const System::String &urlOrBookmark, bool isBookmark)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| displayText | const System::String\& | Text des Links, der im Dokument angezeigt werden soll. |
| urlOrBookmark | const System::String\& | Linkziel. Kann eine URL oder ein Name eines Lesezeichens im Dokument sein. Diese Methode fügt der URL immer Anführungszeichen am Anfang und Ende hinzu. |
| isBookmark | bool | **true** wenn der vorherige Parameter ein Name eines Lesezeichens im Dokument ist; **false** wenn der vorherige Parameter eine URL ist. |

### ReturnValue

Ein [Field](../../../aspose.words.fields/field/)-Objekt, das das eingefügte Feld darstellt.
## Hinweise


Beachten Sie, dass Sie die Schriftformatierung für den Anzeigetext des Hyperlinks explizit über die [Font](../get_font/) Eigenschaft angeben müssen.

Diese Methode ruft intern [InsertField()](../) auf, um ein MS Word HYPERLINK-Feld in das Dokument einzufügen.

## Beispiele



Zeigt, wie man ein Hyperlink-Feld einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"For more information, please visit the ");

// Fügen Sie einen Hyperlink ein und heben Sie ihn mit benutzerdefinierter Formatierung hervor.
// Der Hyperlink wird ein anklickbarer Text sein, der uns zu dem in der URL angegebenen Ort führt.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
builder->InsertHyperlink(u"Google website", u"https://www.google.com", false);
builder->get_Font()->ClearFormatting();
builder->Writeln(u".");

// Strg + Linksklick auf den Link im Text in Microsoft Word öffnet die URL in einem neuen Webbrowser-Fenster.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlink.docx");
```


Zeigt, wie man den Formatierungsstapel eines Document Builders verwendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Richten Sie die Schriftformatierung ein und schreiben Sie dann den Text, der vor dem Hyperlink steht.
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Size(24);
builder->Write(u"To visit Google, hold Ctrl and click ");

// Behalte unsere aktuelle Formatierungskonfiguration im Stack bei.
builder->PushFont();

// Ändere die aktuelle Formatierung des Builders, indem du einen neuen Stil anwendest.
builder->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Hyperlink);
builder->InsertHyperlink(u"here", u"http://www.google.com", false);

ASSERT_EQ(System::Drawing::Color::get_Blue().ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::Single, builder->get_Font()->get_Underline());

// Stelle die zuvor gespeicherte Schriftformatierung wieder her und entferne das Element aus dem Stack.
builder->PopFont();

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::None, builder->get_Font()->get_Underline());

builder->Write(u". We hope you enjoyed the example.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.PushPopFont.docx");
```


Zeigt, wie man einen Hyperlink einfügt, der auf ein lokales Lesezeichen verweist.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartBookmark(u"Bookmark1");
builder->Write(u"Bookmarked text. ");
builder->EndBookmark(u"Bookmark1");
builder->Writeln(u"Text outside of the bookmark.");

// Fügen Sie ein HYPERLINK-Feld ein, das auf das Lesezeichen verweist. Wir können Feldschalter übergeben
// zur "InsertHyperlink"-Methode als Teil des Arguments, das den Namen des referenzierten Lesezeichens enthält.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
auto hyperlink = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertHyperlink(u"Link to Bookmark1", u"Bookmark1", true));
hyperlink->set_ScreenTip(u"Hyperlink Tip");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

## Siehe auch

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
