---
title: "Aspose::Words::Loading::RtfLoadOptions::RtfLoadOptions constructeur"
linktitle: "RtfLoadOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Loading::RtfLoadOptions::RtfLoadOptions constructor. Initialise une nouvelle instance de cette classe avec les valeurs par défaut en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.loading/rtfloadoptions/rtfloadoptions/
---
## RtfLoadOptions::RtfLoadOptions constructor


Initialise une nouvelle instance de cette classe avec les valeurs par défaut.

```cpp
Aspose::Words::Loading::RtfLoadOptions::RtfLoadOptions()
```


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
