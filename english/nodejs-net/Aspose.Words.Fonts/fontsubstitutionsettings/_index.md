---
title: FontSubstitutionSettings class
linktitle: FontSubstitutionSettings class
articleTitle: FontSubstitutionSettings class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Fonts.FontSubstitutionSettings class. Specifies font substitution mechanism settings"
type: docs
weight: 200
url: /nodejs-net/Aspose.Words.Fonts/fontsubstitutionsettings/
---

## FontSubstitutionSettings class

Specifies font substitution mechanism settings.
To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/nodejs-net/working-with-fonts/) documentation article.




### Remarks

Font substitution process consists of several rules which are checked one by one in specific order.
If the first rule can't resolve the font then second rule is checked and so on.

The order of the rules is following:
1. Font name substitution rule (enabled by default)
2. Font config substitution rule (disabled by default)
3. Table substitution rule (enabled by default)
4. Font info substitution rule (enabled by default)
5. Default font rule (enabled by default)

Note that font info substitution rule will always resolve the font if [FontInfo](../fontinfo/) is available
and will override the default font rule. If you want to use the default font rule then you should disable the
font info substitution rule. 


Note that font config substitution rule will resolve the font in most cases and thus overrides all other rules.




### Properties

| Name | Description |
| --- | --- |
| [defaultFontSubstitution](./defaultFontSubstitution/) | Settings related to default font substitution rule. |
| [fontConfigSubstitution](./fontConfigSubstitution/) | Settings related to font config substitution rule. |
| [fontInfoSubstitution](./fontInfoSubstitution/) | Settings related to font info substitution rule. |
| [fontNameSubstitution](./fontNameSubstitution/) | Settings related to font name substitution rule. |
| [tableSubstitution](./tableSubstitution/) | Settings related to table substitution rule. |

### See Also

* module [Aspose.Words.Fonts](../)

