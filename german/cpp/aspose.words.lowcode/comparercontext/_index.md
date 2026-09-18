---
title: "Aspose::Words::LowCode::ComparerContext class"
linktitle: "ComparerContext"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::LowCode::ComparerContext class. Dokumentvergleichskontext in C++."
type: docs
weight: 550
url: /de/cpp/aspose.words.lowcode/comparercontext/
---
## ComparerContext class


[Document](../../aspose.words/document/) comparer context.

```cpp
class ComparerContext : public Aspose::Words::LowCode::ProcessorContext
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [ComparerContext](./comparercontext/)() |  |
| [get_AcceptRevisions](./get_acceptrevisions/)() const | Gibt an, ob Revisionen in den Dokumenten vor dem Vergleich akzeptiert werden sollen. Wenn die zu vergleichenden Dokumente Revisionen enthalten und dieses Flag auf false gesetzt ist, wird der Prozessor Revisionen ablehnen. Standardwert ist **true**. |
| [get_Author](./get_author/)() const | Der Autor, der den während des Dokumentvergleichs erstellten Revisionen zugewiesen wird. |
| [get_CompareOptions](./get_compareoptions/)() const | Optionen, die beim Vergleich von Dokumenten verwendet werden. |
| [get_DateTime](./get_datetime/)() const | Datum und Uhrzeit, die den während des Dokumentvergleichs erstellten Revisionen zugewiesen werden. |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | [Font](../../aspose.words/font/) Einstellungen, die vom Prozessor verwendet werden. |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | [Document](../../aspose.words/document/) Layout-Optionen, die vom Prozessor verwendet werden. |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | Warnungs-Callback, der vom Prozessor verwendet wird. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [set_AcceptRevisions](./set_acceptrevisions/)(bool) | Gibt an, ob Revisionen in den Dokumenten vor dem Vergleich akzeptiert werden sollen. Wenn die zu vergleichenden Dokumente Revisionen enthalten und dieses Flag auf false gesetzt ist, wird der Prozessor Revisionen ablehnen. Standardwert ist **true**. |
| [set_Author](./set_author/)(const System::String\&) | Der Autor, der den während des Dokumentvergleichs erstellten Revisionen zugewiesen wird. |
| [set_DateTime](./set_datetime/)(System::DateTime) | Datum und Uhrzeit, die den während des Dokumentvergleichs erstellten Revisionen zugewiesen werden. |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | [Font](../../aspose.words/font/) Einstellungen, die vom Prozessor verwendet werden. |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Warnungs-Callback, der vom Prozessor verwendet wird. |
| static [Type](./type/)() |  |
## Siehe auch

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
