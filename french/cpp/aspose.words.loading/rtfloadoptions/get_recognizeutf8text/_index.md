---
title: "Aspose::Words::Loading::RtfLoadOptions::get_RecognizeUtf8Text méthode"
linktitle: "get_RecognizeUtf8Text"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Loading::RtfLoadOptions::get_RecognizeUtf8Text méthode. Lorsqu'elle est définie sur true, elle tentera de détecter les caractères UTF8, qui seront conservés lors de l'importation en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.loading/rtfloadoptions/get_recognizeutf8text/
---
## RtfLoadOptions::get_RecognizeUtf8Text method


Lorsqu'il est réglé sur **true**, il essaiera de détecter les caractères UTF8, qui seront préservés lors de l'importation.

```cpp
bool Aspose::Words::Loading::RtfLoadOptions::get_RecognizeUtf8Text() const
```

## Remarques


La valeur par défaut est **false**.

## Exemples



Montre comment détecter les caractères UTF-8 lors du chargement d'un document RTF.
```cpp
// Créez un objet "RtfLoadOptions" pour modifier la façon dont nous chargeons un document RTF.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::RtfLoadOptions>();

// Définissez la propriété "RecognizeUtf8Text" sur "false" pour supposer que le document utilise le jeu de caractères ISO 8859-1
// et charge chaque caractère du document.
// Définissez la propriété "RecognizeUtf8Text" sur "true" pour analyser tout caractère de longueur variable pouvant apparaître dans le texte.
loadOptions->set_RecognizeUtf8Text(recognizeUtf8Text);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"UTF-8 characters.rtf", loadOptions);

ASSERT_EQ(recognizeUtf8Text ? System::String(u"“John Doe´s list of currency symbols”™\r") + u"€, ¢, £, ¥, ¤" : System::String(u"â€œJohn DoeÂ´s list of currency symbolsâ€\u009dâ„¢\r") + u"â‚¬, Â¢, Â£, Â¥, Â¤", doc->get_FirstSection()->get_Body()->GetText().Trim());
```

## Voir aussi

* Class [RtfLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
