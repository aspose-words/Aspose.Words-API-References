---
title: "Aspose::Words::Fields::FormField::get_TextInputDefault-Methode"
linktitle: "get_TextInputDefault"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FormField::get_TextInputDefault-Methode. Gibt die Standardzeichenkette oder einen Berechnungsausdruck eines Textformularfelds in C++ zurück oder legt sie fest."
type: docs
weight: 21000
url: /de/cpp/aspose.words.fields/formfield/get_textinputdefault/
---
## FormField::get_TextInputDefault method


Liest oder setzt die Standardzeichenkette oder einen Berechnungsausdruck eines Text-Formularfelds.

```cpp
System::String Aspose::Words::Fields::FormField::get_TextInputDefault()
```

## Hinweise


Die Bedeutung dieser Eigenschaft hängt vom Wert der [TextInputType](../get_textinputtype/)‑Eigenschaft ab.

Wenn [TextInputType](../get_textinputtype/) **Regular** oder [Number](../../textformfieldtype/) ist, gibt dieser String die Standardzeichenfolge für das Textformularfeld an. Dieser String ist der Inhalt, den Microsoft Word im Dokument anzeigt, wenn das Formularfeld leer ist.

Wenn [TextInputType](../get_textinputtype/) **Calculated** ist, enthält dieser String den auszuwertenden Ausdruck. Der Ausdruck muss eine Formel sein, die den Anforderungen der Microsoft‑Word‑Formelfeldsyntax entspricht. Wenn Sie über diese Eigenschaft einen neuen Ausdruck festlegen, berechnet Aspose.Words das Formelresultat automatisch und fügt es in das Formularfeld ein.

Microsoft Word erlaubt Zeichenfolgen mit höchstens 255 Zeichen.
## Siehe auch

* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
