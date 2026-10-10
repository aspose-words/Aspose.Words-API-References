---
title: "Aspose::Words::DocumentBase::ImportNode Methode"
linktitle: "ImportNode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBase::ImportNode Methode. Importiert einen Knoten aus einem anderen Dokument in das aktuelle Dokument in C++."
type: docs
weight: 12000
url: /de/cpp/aspose.words/documentbase/importnode/
---
## DocumentBase::ImportNode(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Importiert einen Knoten aus einem anderen Dokument in das aktuelle Dokument.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBase::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Der zu importierende Knoten. |
| isImportChildren | bool | **true** um alle untergeordneten Knoten rekursiv zu importieren; andernfalls **false**. |

### ReturnValue

Der geklonte Knoten, der zum aktuellen Dokument gehört.
## Hinweise


Diese Methode verwendet die Option [UseDestinationStyles](../../importformatmode/), um die Formatierung aufzulösen.

Das Importieren eines Knotens erstellt eine Kopie des Quellknotens, die zum importierenden Dokument gehört. Der zurückgegebene Knoten hat keinen Elternknoten. Der Quellknoten wird nicht verändert oder aus dem Originaldokument entfernt.

Bevor ein Knoten aus einem anderen Dokument in dieses Dokument eingefügt werden kann, muss er importiert werden. Während des Imports werden dokumentbezogene Eigenschaften wie Verweise auf Stile und Listen vom Original in das importierende Dokument übersetzt. Nachdem der Knoten importiert wurde, kann er an die passende Stelle im Dokument eingefügt werden, indem man [InsertBefore1()</see> oder <see cref=\"Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)\">InsertAfter1()](../) verwendet.

Wenn der Quellknoten bereits zum Ziel‑Dokument gehört, wird einfach ein tiefer Klon des Quellknotens erstellt.

## Beispiele



Zeigt, wie man einen Knoten von einem Dokument in ein anderes importiert.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto dstDoc = System::MakeObject<Aspose::Words::Document>();

srcDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(srcDoc, u"Source document first paragraph text."));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(dstDoc, u"Destination document first paragraph text."));

// Jeder Knoten hat ein übergeordnetes Dokument, das das Dokument ist, das den Knoten enthält.
// Das Einfügen eines Knotens in ein Dokument, zu dem der Knoten nicht gehört, löst eine Ausnahme aus.
ASPOSE_ASSERT_NE(dstDoc, srcDoc->get_FirstSection()->get_Document());
ASSERT_THROW(static_cast<std::function<void()>>([&dstDoc, &srcDoc]() -> void
{
    dstDoc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(srcDoc->get_FirstSection());
})(), System::ArgumentException);

// Verwenden Sie die ImportNode-Methode, um eine Kopie eines Knotens zu erstellen, die das Dokument
// das die ImportNode-Methode aufruft, als sein neues Eigentümerdokument festlegt.
auto importedSection = System::ExplicitCast<Aspose::Words::Section>(dstDoc->ImportNode(srcDoc->get_FirstSection(), true));

ASPOSE_ASSERT_EQ(dstDoc, importedSection->get_Document());

// Wir können jetzt den Knoten in das Dokument einfügen.
dstDoc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(importedSection);

ASSERT_EQ(u"Destination document first paragraph text.\r\nSource document first paragraph text.\r\n", dstDoc->ToString(Aspose::Words::SaveFormat::Text));
```

## Siehe auch

* Class [Node](../../node/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBase::ImportNode(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode) method


Importiert einen Knoten aus einem anderen Dokument in das aktuelle Dokument mit einer Option zur Steuerung der Formatierung.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBase::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren, Aspose::Words::ImportFormatMode importFormatMode)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Der zu importierende Knoten. |
| isImportChildren | bool | **true** um alle untergeordneten Knoten rekursiv zu importieren; andernfalls **false**. |
| importFormatMode | Aspose::Words::ImportFormatMode | Gibt an, wie sich widersprechende Formatierungen zusammengeführt werden. |

### ReturnValue

Der geklonte, importierte Knoten. Der Knoten gehört zum Ziel-Dokument, hat aber keinen übergeordneten Knoten.
## Hinweise


Diese Überladung ist nützlich, um zu steuern, wie Stile und Listformatierungen importiert werden.

Das Importieren eines Knotens erstellt eine Kopie des Quellknotens, die zum importierenden Dokument gehört. Der zurückgegebene Knoten hat keinen Elternknoten. Der Quellknoten wird nicht verändert oder aus dem Originaldokument entfernt.

Bevor ein Knoten aus einem anderen Dokument in dieses Dokument eingefügt werden kann, muss er importiert werden. Während des Imports werden dokumentbezogene Eigenschaften wie Verweise auf Stile und Listen vom Original in das importierende Dokument übersetzt. Nachdem der Knoten importiert wurde, kann er an die passende Stelle im Dokument eingefügt werden, indem man [InsertBefore1()</see> oder <see cref=\"Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)\">InsertAfter1()](../) verwendet.

Wenn der Quellknoten bereits zum Ziel‑Dokument gehört, wird einfach ein tiefer Klon des Quellknotens erstellt.

## Beispiele



Zeigt, wie man einen Knoten vom Quelldokument zum Zieldokument mit bestimmten Optionen importiert.
```cpp
// Erstellen Sie zwei Dokumente und fügen Sie jedem Dokument einen Zeichenstil hinzu.
// Konfigurieren Sie die Stile so, dass sie denselben Namen, aber unterschiedliche Textformatierungen haben.
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Style> srcStyle = srcDoc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"My style");
srcStyle->get_Font()->set_Name(u"Courier New");
auto srcBuilder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);
srcBuilder->get_Font()->set_Style(srcStyle);
srcBuilder->Writeln(u"Source document text.");

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Style> dstStyle = dstDoc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"My style");
dstStyle->get_Font()->set_Name(u"Calibri");
auto dstBuilder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
dstBuilder->get_Font()->set_Style(dstStyle);
dstBuilder->Writeln(u"Destination document text.");

// Importieren Sie den Abschnitt vom Zieldokument in das Quelldokument, was zu einer Stilnamenskollision führt.
// Wenn wir Zielstile verwenden, dann wird der importierte Quelltext mit demselben Stilsnamen
// wie der Zieltext den Zielstil übernimmt.
auto importedSection = System::ExplicitCast<Aspose::Words::Section>(dstDoc->ImportNode(srcDoc->get_FirstSection(), true, Aspose::Words::ImportFormatMode::UseDestinationStyles));
ASSERT_EQ(dstStyle->get_Font()->get_Name(), importedSection->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Name());
ASSERT_EQ(dstStyle->get_Name(), importedSection->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_StyleName());

// Wenn wir ImportFormatMode.KeepDifferentStyles verwenden, wird der Quellstil beibehalten,
// und der Namenskonflikt wird durch Hinzufügen eines Suffixes gelöst.
dstDoc->ImportNode(srcDoc->get_FirstSection(), true, Aspose::Words::ImportFormatMode::KeepDifferentStyles);
ASSERT_EQ(dstStyle->get_Font()->get_Name(), dstDoc->get_Styles()->idx_get(u"My style")->get_Font()->get_Name());
ASSERT_EQ(srcStyle->get_Font()->get_Name(), dstDoc->get_Styles()->idx_get(u"My style_0")->get_Font()->get_Name());
```

## Siehe auch

* Class [Node](../../node/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBase::ImportNode(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) method


Importiert einen Knoten aus einem anderen Dokument in das aktuelle Dokument mit einer Option zur Steuerung der Formatierung.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBase::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Der zu importierende Knoten. |
| isImportChildren | bool | **true** um alle untergeordneten Knoten rekursiv zu importieren; andernfalls **false**. |
| importFormatMode | Aspose::Words::ImportFormatMode | Gibt an, wie sich widersprechende Formatierungen zusammengeführt werden. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | Ermöglicht das Angeben verschiedener zusätzlicher Formatierungsoptionen. |

### ReturnValue

Der geklonte, importierte Knoten. Der Knoten gehört zum Ziel-Dokument, hat aber keinen übergeordneten Knoten.
## Hinweise


Diese Überladung ist nützlich, um zu steuern, wie Stile und Listformatierungen importiert werden.

Das Importieren eines Knotens erstellt eine Kopie des Quellknotens, die zum importierenden Dokument gehört. Der zurückgegebene Knoten hat keinen Elternknoten. Der Quellknoten wird nicht verändert oder aus dem Originaldokument entfernt.

Bevor ein Knoten aus einem anderen Dokument in dieses Dokument eingefügt werden kann, muss er importiert werden. Während des Imports werden dokumentbezogene Eigenschaften wie Verweise auf Stile und Listen vom Original in das importierende Dokument übersetzt. Nachdem der Knoten importiert wurde, kann er an die passende Stelle im Dokument eingefügt werden, indem man [InsertBefore1()</see> oder <see cref=\"Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)\">InsertAfter1()](../) verwendet.

Wenn der Quellknoten bereits zum Ziel‑Dokument gehört, wird einfach ein tiefer Klon des Quellknotens erstellt.

## Beispiele



Zeigt, wie man einen Knoten importiert, wobei die Quellthemenfarben von Formen aufgelöst werden.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);

// Wechseln Sie zur primären Fußzeile und fügen Sie eine Form ein, die Themenfarben verwendet.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 50);
shape->get_Stroke()->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
// Importieren Sie die Quellfußzeile in das Zieldokument, wobei die Themenfarben aufgelöst werden,
// so dass die Form ihre tatsächliche Farbe aus dem Quelldokument beibehält.
System::SharedPtr<Aspose::Words::HeaderFooter> footer = srcDoc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_ResolveThemeColors(true);
auto importedFooter = System::ExplicitCast<Aspose::Words::HeaderFooter>(dstDoc->ImportNode(footer, true, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options));

dstDoc->get_FirstSection()->get_HeadersFooters()->Add(importedFooter);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBase.ImportNodeWithResolveThemeColors.docx");
```

## Siehe auch

* Class [Node](../../node/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
