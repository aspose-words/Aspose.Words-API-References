---
title: CleanupOptions.SymbolicFonts
linktitle: SymbolicFonts
articleTitle: SymbolicFonts
second_title: Aspose.Words for .NET
description: CleanupOptions SymbolicFonts property. Specifies that symbolic fonts Symbol Wingdings etc... should be replaced using appropriate Unicode fonts. Default value is false.
type: docs
weight: 30
url: /net/aspose.words/cleanupoptions/symbolicfonts/
---
## CleanupOptions.SymbolicFonts property

Specifies that symbolic fonts (Symbol, Wingdings, etc...) should be replaced using appropriate Unicode fonts. Default value is `false`.

```csharp
public bool SymbolicFonts { get; set; }
```

## Examples

Shows how to replace text formatted with symbolic fonts (Symbol, Wingdings, etc.) with Unicode text.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Symbolic fonts display characters with glyphs of their own. For example, the "Symbol" font
// displays the U+F057 character as "Ω", so the text loses its meaning without the font.
string[] symbolicFonts = { "Symbol", "Wingdings" };
string Describe(Run run) =>
    $"\"{run.Text}\" ({string.Join(" ", run.Text.Select(c => $"U+{(int)c:X4}"))}), font \"{run.Font.Name}\"";

List<Paragraph> paragraphs = new List<Paragraph>();
foreach (Run run in doc.GetChildNodes(NodeType.Run, true))
{
    if (!symbolicFonts.Contains(run.Font.Name))
        continue;

    Console.WriteLine($"Before: {Describe(run)}");
    if (!paragraphs.Contains(run.ParentParagraph))
        paragraphs.Add(run.ParentParagraph);
}

// Replace the symbolic text with the equivalent Unicode text formatted with appropriate Unicode fonts.
CleanupOptions cleanupOptions = new CleanupOptions { SymbolicFonts = true };
doc.Cleanup(cleanupOptions);

// The same paragraphs now show the symbols as regular Unicode characters, for example, "Ω" is U+03A9.
foreach (Paragraph paragraph in paragraphs)
    foreach (Run run in paragraph.Runs)
        if (run.Text.Any(c => c > 0x7F))
            Console.WriteLine($"After: {Describe(run)}");

doc.Save(ArtifactsDir + "CleanupOptions.SymbolicFonts.docx");
```

### See Also

* class [CleanupOptions](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
