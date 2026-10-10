---
title: "Aspose::Words::Section::ClearHeadersFooters Methode"
linktitle: "ClearHeadersFooters"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Section::ClearHeadersFooters method. Löscht die Kopf- und Fußzeilen dieses Abschnitts in C++."
type: docs
weight: 6000
url: /de/cpp/aspose.words/section/clearheadersfooters/
---
## Section::ClearHeadersFooters() method


Löscht die Kopf- und Fußzeilen dieses Abschnitts.

```cpp
void Aspose::Words::Section::ClearHeadersFooters()
```

## Hinweise


Der Text aller Kopf- und Fußzeilen wird gelöscht, aber die [HeaderFooter](../../headerfooter/)-Objekte selbst werden nicht entfernt.

Dadurch werden die Kopf- und Fußzeilen dieses Abschnitts mit den Kopf- und Fußzeilen des vorherigen Abschnitts verknüpft.

## Beispiele



Zeigt, wie man den Inhalt aller Kopf- und Fußzeilen in einem Abschnitt löscht.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_EQ(0, doc->get_FirstSection()->get_HeadersFooters()->get_Count());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"This is the primary header.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Writeln(u"This is the primary footer.");

ASSERT_EQ(2, doc->get_FirstSection()->get_HeadersFooters()->get_Count());

ASSERT_EQ(u"This is the primary header.", doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetText().Trim());
ASSERT_EQ(u"This is the primary footer.", doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetText().Trim());

// Leert alle Kopf- und Fußzeilen in diesem Abschnitt von ihrem gesamten Inhalt.
// Die Kopf- und Fußzeilen selbst bleiben erhalten, zeigen jedoch nichts an.
doc->get_FirstSection()->ClearHeadersFooters();

ASSERT_EQ(2, doc->get_FirstSection()->get_HeadersFooters()->get_Count());

ASSERT_EQ(System::String::Empty, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetText().Trim());
ASSERT_EQ(System::String::Empty, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetText().Trim());
```

## Siehe auch

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Section::ClearHeadersFooters(bool) method


Löscht die Kopf- und Fußzeilen dieses Abschnitts.

```cpp
void Aspose::Words::Section::ClearHeadersFooters(bool preserveWatermarks)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| preserveWatermarks | bool | True, wenn die Wasserzeichen nicht entfernt werden sollen. |
## Hinweise


Der Text aller Kopf- und Fußzeilen wird gelöscht, aber die [HeaderFooter](../../headerfooter/)-Objekte selbst werden nicht entfernt.

Dadurch werden die Kopf- und Fußzeilen dieses Abschnitts mit den Kopf- und Fußzeilen des vorherigen Abschnitts verknüpft.

## Beispiele



Zeigt, wie man den Inhalt von Kopf- und Fußzeile mit oder ohne Wasserzeichen löscht.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// Fügen Sie ein Wasserzeichen als Klartext hinzu.
doc->get_Watermark()->SetText(u"Aspose Watermark");

// Stellen Sie sicher, dass die Kopf- und Fußzeilen Inhalt haben.
System::SharedPtr<Aspose::Words::HeaderFooterCollection> headersFooters = doc->get_FirstSection()->get_HeadersFooters();
ASSERT_EQ(u"First header", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderFirst)->GetText().Trim());
ASSERT_EQ(u"Second header", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderEven)->GetText().Trim());
ASSERT_EQ(u"Third header", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetText().Trim());
ASSERT_EQ(u"First footer", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterFirst)->GetText().Trim());
ASSERT_EQ(u"Second footer", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterEven)->GetText().Trim());
ASSERT_EQ(u"Third footer", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetText().Trim());

// Entfernt allen Kopf- und Fußzeileninhalt außer den Wasserzeichen.
doc->get_FirstSection()->ClearHeadersFooters(true);

headersFooters = doc->get_FirstSection()->get_HeadersFooters();
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderFirst)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderEven)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterFirst)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterEven)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetText().Trim());
ASSERT_EQ(Aspose::Words::WatermarkType::Text, doc->get_Watermark()->get_Type());

// Entfernt allen Kopf- und Fußzeileninhalt einschließlich der Wasserzeichen.
doc->get_FirstSection()->ClearHeadersFooters(false);
ASSERT_EQ(Aspose::Words::WatermarkType::None, doc->get_Watermark()->get_Type());
```

## Siehe auch

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
