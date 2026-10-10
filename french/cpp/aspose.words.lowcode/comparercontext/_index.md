---
title: "Aspose::Words::LowCode::ComparerContext classe"
linktitle: "ComparerContext"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::LowCode::ComparerContext classe. Contexte de comparaison de documents en C++."
type: docs
weight: 550
url: /fr/cpp/aspose.words.lowcode/comparercontext/
---
## ComparerContext class


[Document](../../aspose.words/document/) comparer context.

```cpp
class ComparerContext : public Aspose::Words::LowCode::ProcessorContext
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [ComparerContext](./comparercontext/)() |  |
| [get_AcceptRevisions](./get_acceptrevisions/)() const | Indique s'il faut accepter les révisions dans les documents avant de les comparer. Si les documents comparés contiennent des révisions et que ce drapeau est défini sur false, le processeur rejettera les révisions. La valeur par défaut est **true**. |
| [get_Author](./get_author/)() const | L'auteur à attribuer aux révisions créées lors de la comparaison de documents. |
| [get_CompareOptions](./get_compareoptions/)() const | Options utilisées lors de la comparaison de documents. |
| [get_DateTime](./get_datetime/)() const | La date et l'heure attribuées aux révisions créées lors de la comparaison de documents. |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | Paramètres de [Police](../../aspose.words/font/) utilisés par le processeur. |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | Options de mise en page du [Document](../../aspose.words/document/) utilisées par le processeur. |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | Rappel d'avertissement utilisé par le processeur. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [set_AcceptRevisions](./set_acceptrevisions/)(bool) | Indique s'il faut accepter les révisions dans les documents avant de les comparer. Si les documents comparés contiennent des révisions et que ce drapeau est défini sur false, le processeur rejettera les révisions. La valeur par défaut est **true**. |
| [set_Author](./set_author/)(const System::String\&) | L'auteur à attribuer aux révisions créées lors de la comparaison de documents. |
| [set_DateTime](./set_datetime/)(System::DateTime) | La date et l'heure attribuées aux révisions créées lors de la comparaison de documents. |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Paramètres de [Police](../../aspose.words/font/) utilisés par le processeur. |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Rappel d'avertissement utilisé par le processeur. |
| static [Type](./type/)() |  |
## Voir aussi

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
