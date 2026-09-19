---
title: "Aspose::Words::ImportFormatOptions class"
linktitle: "ImportFormatOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::ImportFormatOptions class. Consente di specificare varie opzioni di importazione per formattare l'output. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 35000
url: /it/cpp/aspose.words/importformatoptions/
---
## ImportFormatOptions class


Consente di specificare varie opzioni di importazione per formattare l'output. Per saperne di più, visita l'articolo di documentazione [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/).

```cpp
class ImportFormatOptions : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_AdjustSentenceAndWordSpacing](./get_adjustsentenceandwordspacing/)() const | Ottiene o imposta un valore booleano che specifica se regolare automaticamente la spaziatura di frasi e parole. Il valore predefinito è **false**. |
| [get_AppendDocumentWithNewPage](./get_appenddocumentwithnewpage/)() const | Ottiene o imposta un valore booleano che indica se modificare forzatamente il tipo della prima sezione importata in [NewPage](../sectionstart/) quando si chiama [AppendDocument()](../). Il valore predefinito è **true**. |
| [get_ForceCopyStyles](./get_forcecopystyles/)() const | Ottiene o imposta un valore booleano che indica se copiare gli stili in conflitto nella modalità [KeepSourceFormatting](../importformatmode/). Il valore predefinito è **false**. |
| [get_IgnoreHeaderFooter](./get_ignoreheaderfooter/)() const | Ottiene o imposta un valore booleano che specifica che la formattazione di origine del contenuto intestazioni/piè di pagina viene ignorata se si utilizza la modalità [KeepSourceFormatting](../importformatmode/). Il valore predefinito è **true**. |
| [get_IgnoreTextBoxes](./get_ignoretextboxes/)() const | Ottiene o imposta un valore booleano che specifica che la formattazione di origine del contenuto delle caselle di testo viene ignorata se si utilizza la modalità [KeepSourceFormatting](../importformatmode/). Il valore predefinito è **true**. |
| [get_KeepSourceNumbering](./get_keepsourcenumbering/)() const | Ottiene o imposta un valore booleano che specifica come verrà importata la numerazione quando entra in conflitto nei documenti di origine e destinazione. Il valore predefinito è **false**. |
| [get_MergePastedLists](./get_mergepastedlists/)() const | Ottiene o imposta un valore booleano che specifica se gli elenchi incollati verranno uniti agli elenchi circostanti. Il valore predefinito è **false**. |
| [get_ResolveThemeColors](./get_resolvethemecolors/)() const | Ottiene o imposta un valore booleano che specifica se risolvere forzatamente i colori tema delle forme. Il valore predefinito è **false**. |
| [get_SmartStyleBehavior](./get_smartstylebehavior/)() const | Ottiene o imposta un valore booleano che specifica come verranno importati gli stili quando hanno lo stesso nome nei documenti di origine e destinazione. Il valore predefinito è **false**. |
| [GetType](./gettype/)() const override |  |
| [ImportFormatOptions](./importformatoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AdjustSentenceAndWordSpacing](./set_adjustsentenceandwordspacing/)(bool) | Impostatore per [Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing](./get_adjustsentenceandwordspacing/). |
| [set_AppendDocumentWithNewPage](./set_appenddocumentwithnewpage/)(bool) | Impostatore per [Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage](./get_appenddocumentwithnewpage/). |
| [set_ForceCopyStyles](./set_forcecopystyles/)(bool) | Impostatore per [Aspose::Words::ImportFormatOptions::get_ForceCopyStyles](./get_forcecopystyles/). |
| [set_IgnoreHeaderFooter](./set_ignoreheaderfooter/)(bool) | Impostatore per [Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter](./get_ignoreheaderfooter/). |
| [set_IgnoreTextBoxes](./set_ignoretextboxes/)(bool) | Impostatore per [Aspose::Words::ImportFormatOptions::get_IgnoreTextBoxes](./get_ignoretextboxes/). |
| [set_KeepSourceNumbering](./set_keepsourcenumbering/)(bool) | Impostatore per [Aspose::Words::ImportFormatOptions::get_KeepSourceNumbering](./get_keepsourcenumbering/). |
| [set_MergePastedLists](./set_mergepastedlists/)(bool) | Impostatore per [Aspose::Words::ImportFormatOptions::get_MergePastedLists](./get_mergepastedlists/). |
| [set_ResolveThemeColors](./set_resolvethemecolors/)(bool) | Impostatore per [Aspose::Words::ImportFormatOptions::get_ResolveThemeColors](./get_resolvethemecolors/). |
| [set_SmartStyleBehavior](./set_smartstylebehavior/)(bool) | Impostatore per [Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior](./get_smartstylebehavior/). |
| static [Type](./type/)() |  |

## Esempi



Mostra come risolvere gli stili duplicati durante l'inserimento dei documenti.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);

System::SharedPtr<Aspose::Words::Style> myStyle = builder->get_Document()->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
myStyle->get_Font()->set_Size(14);
myStyle->get_Font()->set_Name(u"Courier New");
myStyle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

builder->get_ParagraphFormat()->set_StyleName(myStyle->get_Name());
builder->Writeln(u"Hello world!");

// Clona il documento e modifica lo stile "MyStyle" del clone, in modo che abbia un colore diverso rispetto a quello originale.
// Se inseriamo il clone nel documento originale, i due stili con lo stesso nome provocheranno un conflitto.
System::SharedPtr<Aspose::Words::Document> srcDoc = dstDoc->Clone();
srcDoc->get_Styles()->idx_get(u"MyStyle")->get_Font()->set_Color(System::Drawing::Color::get_Red());

// Quando abilitiamo SmartStyleBehavior e utilizziamo la modalità di importazione KeepSourceFormatting,
// Aspose.Words risolverà i conflitti di stile convertendo gli stili del documento di origine.
// con gli stessi nomi degli stili di destinazione in attributi di paragrafo diretti.
auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_SmartStyleBehavior(true);

builder->InsertDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.SmartStyleBehavior.docx");
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
