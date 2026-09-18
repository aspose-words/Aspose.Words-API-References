---
title: "Aspose::Words::StyleCollection::AddCopy-Methode"
linktitle: "AddCopy"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::StyleCollection::AddCopy-Methode. Kopiert einen Stil in diese Sammlung in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words/stylecollection/addcopy/
---
## StyleCollection::AddCopy method


Kopiert einen Stil in diese Sammlung.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::AddCopy(const System::SharedPtr<Aspose::Words::Style> &style)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| style | const System::SharedPtr\<Aspose::Words::Style\>\& | [Style](../../style/) zu kopieren. |

### ReturnValue

Kopierter Stil ist einsatzbereit.
## Hinweise


[Style](../../style/) to be copied can belong to the same document as well as to different document.

Verknüpfter Stil wurde kopiert.

Diese Methode kopiert keine Basisstile.

Wenn die Sammlung bereits einen Stil mit demselben Namen enthält, wird ein neuer Name automatisch erzeugt, indem das Suffix \"_number\" ab 0 angehängt wird, z. B. \"Normal_0\", \"Heading 1_1\" usw. Verwenden Sie den [Name](../../style/get_name/) Setter, um den Namen des importierten Stils zu ändern.

## Beispiele



Zeigt, wie man den Stil eines Dokuments klont.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Die AddCopy‑Methode erstellt eine Kopie des angegebenen Stils und
// generiert automatisch einen neuen Namen für den Stil, z. B. "Heading 1_0".
System::SharedPtr<Aspose::Words::Style> newStyle = doc->get_Styles()->AddCopy(doc->get_Styles()->idx_get(u"Heading 1"));

// Verwenden Sie die "Name"‑Eigenschaft des Stils, um den identifizierenden Namen des Stils zu ändern.
newStyle->set_Name(u"My Heading 1");

// Unser Dokument hat jetzt zwei identisch aussehende Stile mit unterschiedlichen Namen.
// Das Ändern der Einstellungen eines der Stile wirkt sich nicht auf den anderen aus.
newStyle->get_Font()->set_Color(System::Drawing::Color::get_Red());

ASSERT_EQ(u"My Heading 1", newStyle->get_Name());
ASSERT_EQ(u"Heading 1", doc->get_Styles()->idx_get(u"Heading 1")->get_Name());

ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Type(), newStyle->get_Type());
ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Name(), newStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Size(), newStyle->get_Font()->get_Size());
ASPOSE_ASSERT_NE(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Color(), newStyle->get_Font()->get_Color());
```


Zeigt, wie ein Stil von einem Dokument in ein anderes Dokument importiert wird.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();

// Erstellen Sie einen benutzerdefinierten Stil für das Quell-Dokument.
System::SharedPtr<Aspose::Words::Style> srcStyle = srcDoc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
srcStyle->get_Font()->set_Color(System::Drawing::Color::get_Red());

// Importieren Sie den benutzerdefinierten Stil des Quelldokuments in das Zieldokument.
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Style> newStyle = dstDoc->get_Styles()->AddCopy(srcStyle);

// Der importierte Stil hat ein Erscheinungsbild, das dem des Quellstils identisch ist.
ASSERT_EQ(u"MyStyle", newStyle->get_Name());
ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), newStyle->get_Font()->get_Color().ToArgb());
```

## Siehe auch

* Class [Style](../../style/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
