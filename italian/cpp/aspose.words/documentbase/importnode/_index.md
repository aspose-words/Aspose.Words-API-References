---
title: "Metodo Aspose::Words::DocumentBase::ImportNode"
linktitle: "ImportNode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::DocumentBase::ImportNode. Importa un nodo da un altro documento al documento corrente in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words/documentbase/importnode/
---
## DocumentBase::ImportNode(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Importa un nodo da un altro documento al documento corrente.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBase::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Il nodo da importare. |
| isImportChildren | bool | **true** per importare tutti i nodi figlio ricorsivamente; altrimenti, **false**. |

### ReturnValue

Il nodo clonato che appartiene al documento corrente.
## Note


Questo metodo utilizza l'opzione [UseDestinationStyles](../../importformatmode/) per risolvere la formattazione.

L'importazione di un nodo crea una copia del nodo sorgente appartenente al documento di destinazione. Il nodo restituito non ha genitore. Il nodo sorgente non viene modificato né rimosso dal documento originale.

Prima che un nodo da un altro documento possa essere inserito in questo documento, deve essere importato. Durante l'importazione, le proprietà specifiche del documento come i riferimenti a stili e elenchi vengono tradotte dall'originale al documento di destinazione. Dopo che il nodo è stato importato, può essere inserito nel punto appropriato del documento utilizzando [InsertBefore1()</see> o <see cref=\"Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertAfter1()](../).

Se il nodo sorgente appartiene già al documento di destinazione, viene semplicemente creata una clonazione profonda del nodo sorgente.

## Esempi



Mostra come importare un nodo da un documento all'altro.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto dstDoc = System::MakeObject<Aspose::Words::Document>();

srcDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(srcDoc, u"Source document first paragraph text."));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(dstDoc, u"Destination document first paragraph text."));

// Ogni nodo ha un documento genitore, che è il documento che contiene il nodo.
// Inserire un nodo in un documento a cui il nodo non appartiene genererà un'eccezione.
ASPOSE_ASSERT_NE(dstDoc, srcDoc->get_FirstSection()->get_Document());
ASSERT_THROW(static_cast<std::function<void()>>([&dstDoc, &srcDoc]() -> void
{
    dstDoc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(srcDoc->get_FirstSection());
})(), System::ArgumentException);

// Utilizza il metodo ImportNode per creare una copia di un nodo, che avrà il documento
// che ha chiamato il metodo ImportNode impostato come suo nuovo documento proprietario.
auto importedSection = System::ExplicitCast<Aspose::Words::Section>(dstDoc->ImportNode(srcDoc->get_FirstSection(), true));

ASPOSE_ASSERT_EQ(dstDoc, importedSection->get_Document());

// Ora possiamo inserire il nodo nel documento.
dstDoc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(importedSection);

ASSERT_EQ(u"Destination document first paragraph text.\r\nSource document first paragraph text.\r\n", dstDoc->ToString(Aspose::Words::SaveFormat::Text));
```

## Vedi anche

* Class [Node](../../node/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBase::ImportNode(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode) method


Importa un nodo da un altro documento al documento corrente con un'opzione per controllare la formattazione.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBase::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren, Aspose::Words::ImportFormatMode importFormatMode)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Il nodo da importare. |
| isImportChildren | bool | **true** per importare tutti i nodi figlio ricorsivamente; altrimenti, **false**. |
| importFormatMode | Aspose::Words::ImportFormatMode | Specifica come unire la formattazione degli stili che entra in conflitto. |

### ReturnValue

Il nodo clonato e importato. Il nodo appartiene al documento di destinazione, ma non ha genitore.
## Note


Questa overload è utile per controllare come vengono importati gli stili e la formattazione degli elenchi.

L'importazione di un nodo crea una copia del nodo sorgente appartenente al documento di destinazione. Il nodo restituito non ha genitore. Il nodo sorgente non viene modificato né rimosso dal documento originale.

Prima che un nodo da un altro documento possa essere inserito in questo documento, deve essere importato. Durante l'importazione, le proprietà specifiche del documento come i riferimenti a stili e elenchi vengono tradotte dall'originale al documento di destinazione. Dopo che il nodo è stato importato, può essere inserito nel punto appropriato del documento utilizzando [InsertBefore1()</see> o <see cref=\"Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertAfter1()](../).

Se il nodo sorgente appartiene già al documento di destinazione, viene semplicemente creata una clonazione profonda del nodo sorgente.

## Esempi



Mostra come importare un nodo dal documento sorgente al documento di destinazione con opzioni specifiche.
```cpp
// Crea due documenti e aggiungi uno stile di carattere a ciascun documento.
// Configura gli stili in modo che abbiano lo stesso nome, ma una formattazione del testo diversa.
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

// Importa la Sezione dal documento di destinazione nel documento sorgente, causando una collisione di nomi di stile.
// Se utilizziamo gli stili di destinazione, allora il testo sorgente importato con lo stesso nome di stile
// come il testo di destinazione adotterà lo stile di destinazione.
auto importedSection = System::ExplicitCast<Aspose::Words::Section>(dstDoc->ImportNode(srcDoc->get_FirstSection(), true, Aspose::Words::ImportFormatMode::UseDestinationStyles));
ASSERT_EQ(dstStyle->get_Font()->get_Name(), importedSection->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Name());
ASSERT_EQ(dstStyle->get_Name(), importedSection->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_StyleName());

// Se utilizziamo ImportFormatMode.KeepDifferentStyles, lo stile sorgente viene preservato,
// e il conflitto di denominazione si risolve aggiungendo un suffisso.
dstDoc->ImportNode(srcDoc->get_FirstSection(), true, Aspose::Words::ImportFormatMode::KeepDifferentStyles);
ASSERT_EQ(dstStyle->get_Font()->get_Name(), dstDoc->get_Styles()->idx_get(u"My style")->get_Font()->get_Name());
ASSERT_EQ(srcStyle->get_Font()->get_Name(), dstDoc->get_Styles()->idx_get(u"My style_0")->get_Font()->get_Name());
```

## Vedi anche

* Class [Node](../../node/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBase::ImportNode(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) method


Importa un nodo da un altro documento al documento corrente con un'opzione per controllare la formattazione.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBase::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Il nodo da importare. |
| isImportChildren | bool | **true** per importare tutti i nodi figlio ricorsivamente; altrimenti, **false**. |
| importFormatMode | Aspose::Words::ImportFormatMode | Specifica come unire la formattazione degli stili che entra in conflitto. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | Consente di specificare varie opzioni di formattazione aggiuntive. |

### ReturnValue

Il nodo clonato e importato. Il nodo appartiene al documento di destinazione, ma non ha genitore.
## Note


Questa overload è utile per controllare come vengono importati gli stili e la formattazione degli elenchi.

L'importazione di un nodo crea una copia del nodo sorgente appartenente al documento di destinazione. Il nodo restituito non ha genitore. Il nodo sorgente non viene modificato né rimosso dal documento originale.

Prima che un nodo da un altro documento possa essere inserito in questo documento, deve essere importato. Durante l'importazione, le proprietà specifiche del documento come i riferimenti a stili e elenchi vengono tradotte dall'originale al documento di destinazione. Dopo che il nodo è stato importato, può essere inserito nel punto appropriato del documento utilizzando [InsertBefore1()</see> o <see cref=\"Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertAfter1()](../).

Se il nodo sorgente appartiene già al documento di destinazione, viene semplicemente creata una clonazione profonda del nodo sorgente.

## Esempi



Mostra come importare un nodo risolvendo i colori del tema sorgente delle forme.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);

// Sposta al piè di pagina principale e inserisci una forma che utilizza i colori del tema.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 50);
shape->get_Stroke()->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
// Importa il piè di pagina di origine nel documento di destinazione con i colori del tema risolti,
// in modo che la forma conservi il suo colore reale dal documento di origine.
System::SharedPtr<Aspose::Words::HeaderFooter> footer = srcDoc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_ResolveThemeColors(true);
auto importedFooter = System::ExplicitCast<Aspose::Words::HeaderFooter>(dstDoc->ImportNode(footer, true, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options));

dstDoc->get_FirstSection()->get_HeadersFooters()->Add(importedFooter);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBase.ImportNodeWithResolveThemeColors.docx");
```

## Vedi anche

* Class [Node](../../node/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
