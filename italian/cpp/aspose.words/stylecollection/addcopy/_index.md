---
title: "Aspose::Words::StyleCollection::AddCopy metodo"
linktitle: "AddCopy"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::StyleCollection::AddCopy metodo. Copia uno stile in questa collezione in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words/stylecollection/addcopy/
---
## StyleCollection::AddCopy method


Copia uno stile in questa raccolta.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::AddCopy(const System::SharedPtr<Aspose::Words::Style> &style)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| style | const System::SharedPtr\<Aspose::Words::Style\>\& | [Style](../../style/) da copiare. |

### ReturnValue

Stile copiato pronto per l'uso.
## Note


[Style](../../style/) to be copied can belong to the same document as well as to different document.

Lo stile collegato è stato copiato.

Questo metodo non copia gli stili di base.

Se la collezione contiene già uno stile con lo stesso nome, allora il nuovo nome viene generato automaticamente aggiungendo il suffisso "_number" a partire da 0, ad esempio "Normal_0", "Heading 1_1" ecc. Usa il setter [Name](../../style/get_name/) per modificare il nome dello stile importato.

## Esempi



Mostra come clonare lo stile di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Il metodo AddCopy crea una copia dello stile specificato e
// genera automaticamente un nuovo nome per lo stile, ad esempio "Heading 1_0".
System::SharedPtr<Aspose::Words::Style> newStyle = doc->get_Styles()->AddCopy(doc->get_Styles()->idx_get(u"Heading 1"));

// Utilizza la proprietà "Name" dello stile per modificare il nome identificativo dello stile.
newStyle->set_Name(u"My Heading 1");

// Il nostro documento ora ha due stili dall'aspetto identico con nomi diversi.
// Modificare le impostazioni di uno dei due stili non influisce sull'altro.
newStyle->get_Font()->set_Color(System::Drawing::Color::get_Red());

ASSERT_EQ(u"My Heading 1", newStyle->get_Name());
ASSERT_EQ(u"Heading 1", doc->get_Styles()->idx_get(u"Heading 1")->get_Name());

ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Type(), newStyle->get_Type());
ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Name(), newStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Size(), newStyle->get_Font()->get_Size());
ASPOSE_ASSERT_NE(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Color(), newStyle->get_Font()->get_Color());
```


Mostra come importare uno stile da un documento a un documento diverso.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();

// Crea uno stile personalizzato per il documento di origine.
System::SharedPtr<Aspose::Words::Style> srcStyle = srcDoc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
srcStyle->get_Font()->set_Color(System::Drawing::Color::get_Red());

// Importa lo stile personalizzato del documento di origine nel documento di destinazione.
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Style> newStyle = dstDoc->get_Styles()->AddCopy(srcStyle);

// Lo stile importato ha un aspetto identico al suo stile di origine.
ASSERT_EQ(u"MyStyle", newStyle->get_Name());
ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), newStyle->get_Font()->get_Color().ToArgb());
```

## Vedi anche

* Class [Style](../../style/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
