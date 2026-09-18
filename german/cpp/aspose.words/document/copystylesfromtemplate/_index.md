---
title: "Aspose::Words::Document::CopyStylesFromTemplate‑Methode"
linktitle: "CopyStylesFromTemplate"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::CopyStylesFromTemplate‑Methode. Kopiert Stile aus der angegebenen Vorlage in ein Dokument in C++."
type: docs
weight: 9000
url: /de/cpp/aspose.words/document/copystylesfromtemplate/
---
## Document::CopyStylesFromTemplate(const System::SharedPtr\<Aspose::Words::Document\>\&) method


Kopiert Formatvorlagen von der angegebenen Vorlage in ein Dokument.

```cpp
void Aspose::Words::Document::CopyStylesFromTemplate(const System::SharedPtr<Aspose::Words::Document> &template_)
```


## Beispiele



Zeigt, wie Stile aus der Vorlage über [Document](../) in ein Dokument kopiert werden.
```cpp
auto template_ = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
auto target = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

target->CopyStylesFromTemplate(template_);
```


Zeigt, wie Stile von einem Dokument in ein anderes kopiert werden.
```cpp
// Erstellen Sie ein Dokument und fügen Sie dann Stile hinzu, die wir in ein anderes Dokument kopieren werden.
auto template_ = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> style = template_->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"TemplateStyle1");
style->get_Font()->set_Name(u"Times New Roman");
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());

style = template_->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"TemplateStyle2");
style->get_Font()->set_Name(u"Arial");
style->get_Font()->set_Color(System::Drawing::Color::get_DeepSkyBlue());

style = template_->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"TemplateStyle3");
style->get_Font()->set_Name(u"Courier New");
style->get_Font()->set_Color(System::Drawing::Color::get_RoyalBlue());

ASSERT_EQ(7, template_->get_Styles()->get_Count());

// Erstellen Sie ein Dokument, in das wir die Stile kopieren werden.
auto target = System::MakeObject<Aspose::Words::Document>();

// Erstellen Sie einen Stil mit demselben Namen wie ein Stil aus dem Vorlagendokument und fügen Sie ihn dem Zieldokument hinzu.
style = target->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"TemplateStyle3");
style->get_Font()->set_Name(u"Calibri");
style->get_Font()->set_Color(System::Drawing::Color::get_Orange());

ASSERT_EQ(5, target->get_Styles()->get_Count());

// Es gibt zwei Möglichkeiten, die Methode aufzurufen, um alle Stile von einem Dokument in ein anderes zu kopieren.
// 1 - Übergabe des Vorlagendokument‑Objekts:
target->CopyStylesFromTemplate(template_);

// Das Kopieren von Stilen fügt alle Stile aus dem Vorlagendokument zum Ziel hinzu
// und überschreibt vorhandene Stile mit demselben Namen.
ASSERT_EQ(7, target->get_Styles()->get_Count());

ASSERT_EQ(u"Courier New", target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Name());
ASSERT_EQ(System::Drawing::Color::get_RoyalBlue().ToArgb(), target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Color().ToArgb());

// 2 - Übergabe des lokalen Systemdateinamens eines Vorlagendokuments:
target->CopyStylesFromTemplate(get_MyDir() + u"Rendering.docx");

ASSERT_EQ(21, target->get_Styles()->get_Count());
```

## Siehe auch

* Class [Document](../)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::CopyStylesFromTemplate(const System::String\&) method


Kopiert Formatvorlagen von der angegebenen Vorlage in ein Dokument.

```cpp
void Aspose::Words::Document::CopyStylesFromTemplate(const System::String &template_)
```


## Beispiele



Zeigt, wie Stile von einem Dokument in ein anderes kopiert werden.
```cpp
// Erstellen Sie ein Dokument und fügen Sie dann Stile hinzu, die wir in ein anderes Dokument kopieren werden.
auto template_ = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> style = template_->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"TemplateStyle1");
style->get_Font()->set_Name(u"Times New Roman");
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());

style = template_->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"TemplateStyle2");
style->get_Font()->set_Name(u"Arial");
style->get_Font()->set_Color(System::Drawing::Color::get_DeepSkyBlue());

style = template_->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"TemplateStyle3");
style->get_Font()->set_Name(u"Courier New");
style->get_Font()->set_Color(System::Drawing::Color::get_RoyalBlue());

ASSERT_EQ(7, template_->get_Styles()->get_Count());

// Erstellen Sie ein Dokument, in das wir die Stile kopieren werden.
auto target = System::MakeObject<Aspose::Words::Document>();

// Erstellen Sie einen Stil mit demselben Namen wie ein Stil aus dem Vorlagendokument und fügen Sie ihn dem Zieldokument hinzu.
style = target->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"TemplateStyle3");
style->get_Font()->set_Name(u"Calibri");
style->get_Font()->set_Color(System::Drawing::Color::get_Orange());

ASSERT_EQ(5, target->get_Styles()->get_Count());

// Es gibt zwei Möglichkeiten, die Methode aufzurufen, um alle Stile von einem Dokument in ein anderes zu kopieren.
// 1 - Übergabe des Vorlagendokument‑Objekts:
target->CopyStylesFromTemplate(template_);

// Das Kopieren von Stilen fügt alle Stile aus dem Vorlagendokument zum Ziel hinzu
// und überschreibt vorhandene Stile mit demselben Namen.
ASSERT_EQ(7, target->get_Styles()->get_Count());

ASSERT_EQ(u"Courier New", target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Name());
ASSERT_EQ(System::Drawing::Color::get_RoyalBlue().ToArgb(), target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Color().ToArgb());

// 2 - Übergabe des lokalen Systemdateinamens eines Vorlagendokuments:
target->CopyStylesFromTemplate(get_MyDir() + u"Rendering.docx");

ASSERT_EQ(21, target->get_Styles()->get_Count());
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
