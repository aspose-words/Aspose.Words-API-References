---
title: Aspose::Words::Fonts::FontNameSubstitutionRule class
linktitle: FontNameSubstitutionRule
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FontNameSubstitutionRule class. Font substitution rule for processing font name. To learn more, visit the Working with Fonts documentation article in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.fonts/fontnamesubstitutionrule/
---
## FontNameSubstitutionRule class


Font substitution rule for processing font name. 
To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) documentation article.

```cpp
class FontNameSubstitutionRule : public FontSubstitutionRule
```

## Methods

| Method | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo \&) const override |  |
| static [Type](./type/)() |  |
| [GetType](../fontsubstitutionrule/gettype/)() const override |  |
| [Is](../fontsubstitutionrule/is/)(const System::TypeInfo \&) const override |  |
| static [Type](../fontsubstitutionrule/type/)() |  |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | Specifies whether the rule is enabled or not. |
| virtual [set_Enabled](../fontsubstitutionrule/set_enabled/)(bool) | Specifies whether the rule is enabled or not. |
## Remarks

 According to this rule Aspose.Words tries to process the font name to get the substitution. Particularly Aspose.Words tries to removes suffixes with '-', ',' and '(' separators like it does the MS Word. 
## See Also

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
