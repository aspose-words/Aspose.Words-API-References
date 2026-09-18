---
title: "Aspose::Words::ImportFormatOptions Klasse"
linktitle: "ImportFormatOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ImportFormatOptions Klasse. Ermöglicht das Festlegen verschiedener Importoptionen zur Formatierung der Ausgabe. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 35000
url: /de/cpp/aspose.words/importformatoptions/
---
## ImportFormatOptions class


Ermöglicht die Angabe verschiedener Importoptionen zur Formatierung der Ausgabe. Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/).

```cpp
class ImportFormatOptions : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_AdjustSentenceAndWordSpacing](./get_adjustsentenceandwordspacing/)() const | Liest oder setzt einen booleschen Wert, der angibt, ob Satz- und Wortabstände automatisch angepasst werden sollen. Der Standardwert ist **false**. |
| [get_AppendDocumentWithNewPage](./get_appenddocumentwithnewpage/)() const | Liest oder setzt einen booleschen Wert, der angibt, ob der Typ des zuerst importierten Abschnitts zum [NewPage](../sectionstart/) zwingend geändert werden soll, wenn [AppendDocument()](../) aufgerufen wird. Der Standardwert ist **true**. |
| [get_ForceCopyStyles](./get_forcecopystyles/)() const | Liest oder setzt einen booleschen Wert, der angibt, ob widersprüchliche Stile im Modus [KeepSourceFormatting](../importformatmode/) kopiert werden sollen. Der Standardwert ist **false**. |
| [get_IgnoreHeaderFooter](./get_ignoreheaderfooter/)() const | Liest oder setzt einen booleschen Wert, der festlegt, dass die Quellformatierung von Kopf‑/Fußzeileninhalten ignoriert wird, wenn der Modus [KeepSourceFormatting](../importformatmode/) verwendet wird. Der Standardwert ist **true**. |
| [get_IgnoreTextBoxes](./get_ignoretextboxes/)() const | Liest oder setzt einen booleschen Wert, der festlegt, dass die Quellformatierung von Textfeld‑Inhalten ignoriert wird, wenn der Modus [KeepSourceFormatting](../importformatmode/) verwendet wird. Der Standardwert ist **true**. |
| [get_KeepSourceNumbering](./get_keepsourcenumbering/)() const | Liest oder setzt einen booleschen Wert, der festlegt, wie die Nummerierung importiert wird, wenn sie in Quell‑ und Zieldokumenten kollidiert. Der Standardwert ist **false**. |
| [get_MergePastedLists](./get_mergepastedlists/)() const | Liest oder setzt einen booleschen Wert, der angibt, ob eingefügte Listen mit umgebenden Listen zusammengeführt werden sollen. Der Standardwert ist **false**. |
| [get_ResolveThemeColors](./get_resolvethemecolors/)() const | Liest oder setzt einen booleschen Wert, der angibt, ob die Themenfarben der Formen zwingend aufgelöst werden sollen. Der Standardwert ist **false**. |
| [get_SmartStyleBehavior](./get_smartstylebehavior/)() const | Liest oder setzt einen booleschen Wert, der festlegt, wie Stile importiert werden, wenn sie in Quell‑ und Zieldokumenten denselben Namen haben. Der Standardwert ist **false**. |
| [GetType](./gettype/)() const override |  |
| [ImportFormatOptions](./importformatoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AdjustSentenceAndWordSpacing](./set_adjustsentenceandwordspacing/)(bool) | Setter für [Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing](./get_adjustsentenceandwordspacing/). |
| [set_AppendDocumentWithNewPage](./set_appenddocumentwithnewpage/)(bool) | Setter für [Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage](./get_appenddocumentwithnewpage/). |
| [set_ForceCopyStyles](./set_forcecopystyles/)(bool) | Setter für [Aspose::Words::ImportFormatOptions::get_ForceCopyStyles](./get_forcecopystyles/). |
| [set_IgnoreHeaderFooter](./set_ignoreheaderfooter/)(bool) | Setter für [Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter](./get_ignoreheaderfooter/). |
| [set_IgnoreTextBoxes](./set_ignoretextboxes/)(bool) | Setter für [Aspose::Words::ImportFormatOptions::get_IgnoreTextBoxes](./get_ignoretextboxes/). |
| [set_KeepSourceNumbering](./set_keepsourcenumbering/)(bool) | Setter für [Aspose::Words::ImportFormatOptions::get_KeepSourceNumbering](./get_keepsourcenumbering/). |
| [set_MergePastedLists](./set_mergepastedlists/)(bool) | Setter für [Aspose::Words::ImportFormatOptions::get_MergePastedLists](./get_mergepastedlists/). |
| [set_ResolveThemeColors](./set_resolvethemecolors/)(bool) | Setter für [Aspose::Words::ImportFormatOptions::get_ResolveThemeColors](./get_resolvethemecolors/). |
| [set_SmartStyleBehavior](./set_smartstylebehavior/)(bool) | Setter für [Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior](./get_smartstylebehavior/). |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie doppelte Formatvorlagen beim Einfügen von Dokumenten aufgelöst werden.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);

System::SharedPtr<Aspose::Words::Style> myStyle = builder->get_Document()->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
myStyle->get_Font()->set_Size(14);
myStyle->get_Font()->set_Name(u"Courier New");
myStyle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

builder->get_ParagraphFormat()->set_StyleName(myStyle->get_Name());
builder->Writeln(u"Hello world!");

// Kopiere das Dokument und bearbeite die "MyStyle"-Formatvorlage der Kopie, sodass sie eine andere Farbe als die des Originals hat.
// Wenn wir die Kopie in das Originaldokument einfügen, führen die beiden Formatvorlagen mit demselben Namen zu einem Konflikt.
System::SharedPtr<Aspose::Words::Document> srcDoc = dstDoc->Clone();
srcDoc->get_Styles()->idx_get(u"MyStyle")->get_Font()->set_Color(System::Drawing::Color::get_Red());

// Wenn wir SmartStyleBehavior aktivieren und den Importformatmodus KeepSourceFormatting verwenden,
// Aspose.Words löst Stilkonflikte, indem es die Formatvorlagen des Quelldokuments konvertiert.
// mit denselben Namen wie Ziel-Formatvorlagen in direkte Absatzattribute umwandelt.
auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_SmartStyleBehavior(true);

builder->InsertDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.SmartStyleBehavior.docx");
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
