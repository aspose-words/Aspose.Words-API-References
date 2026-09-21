---
title: "Aspose::Words::Document::JoinRunsWithSameFormatting metod"
linktitle: "JoinRunsWithSameFormatting"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::JoinRunsWithSameFormatting metod. Sammanfogar körningar med samma formatering i alla stycken i dokumentet i C++."
type: docs
weight: 65000
url: /sv/cpp/aspose.words/document/joinrunswithsameformatting/
---
## Document::JoinRunsWithSameFormatting method


Slår ihop runs med samma formatering i alla stycken i dokumentet.

```cpp
int32_t Aspose::Words::Document::JoinRunsWithSameFormatting()
```


### ReturnValue

Antal sammanslagningar som utförts. När **N** intilliggande körningar sammanfogas räknas de som **N - 1** sammanslagningar.
## Anmärkningar


Detta är en optimeringsmetod. Vissa dokument innehåller intilliggande körningar med samma formatering. Detta sker vanligtvis om ett dokument har redigerats intensivt manuellt. Du kan minska dokumentets storlek och påskynda vidare bearbetning genom att sammanfoga dessa körningar.

Operationen kontrollerar varje [Paragraph](../../paragraph/) nod i dokumentet för intilliggande [Run](../../run/) noder med identiska egenskaper. Den ignorerar unika identifierare som används för att spåra redigeringssessioner för skapande och modifiering av run. Första run i varje sammanslagningssekvens samlar all text. Återstående run tas bort från dokumentet.

## Exempel



Visar hur man slår ihop run i ett dokument för att minska onödiga run.
```cpp
// Öppna ett dokument som innehåller intilliggande run med text med identisk formatering,
// vilket ofta händer om vi redigerar samma stycke flera gånger i Microsoft Word.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Om ett antal av dessa run är intilliggande med identisk formatering,
// kan dokumentet förenklas.
ASSERT_EQ(317, doc->GetChildNodes(Aspose::Words::NodeType::Run, true)->get_Count());

// Kombinera sådana run med denna metod och verifiera antalet run-sammanslagningar som kommer att ske.
ASSERT_EQ(121, doc->JoinRunsWithSameFormatting());

// Antalet sammanslagningar och antalet run vi har efter sammanslagningen
// bör motsvara antalet run vi hade initialt.
ASSERT_EQ(196, doc->GetChildNodes(Aspose::Words::NodeType::Run, true)->get_Count());
```

## Se även

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
