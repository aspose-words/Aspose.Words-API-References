---
title: "Aspose::Words::Fonts::FontSourceBase::get_Priority méthode"
linktitle: "get_Priority"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::FontSourceBase::get_Priority méthode. Retourne la priorité de la source de police en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fonts/fontsourcebase/get_priority/
---
## FontSourceBase::get_Priority method


Renvoie la priorité de la source de police.

```cpp
int32_t Aspose::Words::Fonts::FontSourceBase::get_Priority() const
```

## Remarques


Cette valeur est utilisée lorsqu'il existe des polices avec le même nom de famille et le même style dans différentes sources de polices. Dans ce cas, Aspose.Words sélectionne la police provenant de la source avec la valeur de priorité la plus élevée.

La valeur par défaut est 0.

## Exemples



Montre comment utiliser un fichier de police dans le système de fichiers local comme source de police.
```cpp
auto fileFontSource = System::MakeObject<Aspose::Words::Fonts::FileFontSource>(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({fileFontSource}));

ASSERT_EQ(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", fileFontSource->get_FilePath());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontFile, fileFontSource->get_Type());
ASSERT_EQ(0, fileFontSource->get_Priority());
```

## Voir aussi

* Class [FontSourceBase](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
