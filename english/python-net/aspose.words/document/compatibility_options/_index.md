---
title: Document.compatibility_options property
linktitle: compatibility_options property
articleTitle: compatibility_options property
second_title: Aspose.Words for Python
description: "Document.compatibility_options property. Provides access to document compatibility options (that is, the user preferences entered on the Compatibility tab of the Options dialog in Word)."
type: docs
weight: 50
url: /python-net/aspose.words/document/compatibility_options/
---

## Document.compatibility_options property

Provides access to document compatibility options (that is, the user preferences entered on the **Compatibility**
tab of the **Options** dialog in Word).



```python
@property
def compatibility_options(self) -> aspose.words.settings.CompatibilityOptions:
    ...

```

### Examples

Shows how to optimize the document for different versions of Microsoft Word.

```python
def test_optimize_for(self):

    doc = aw.Document()

    # This object contains an extensive list of flags unique to each document
    # that allow us to facilitate backward compatibility with older versions of Microsoft Word.
    options = doc.compatibility_options

    # Print the default settings for a blank document.
    print("\nDefault optimization settings:")
    ExCompatibilityOptions.print_compatibility_options(options)

    # We can access these settings in Microsoft Word via "File" -> "Options" -> "Advanced" -> "Compatibility options for...".
    doc.save(ARTIFACTS_DIR + "CompatibilityOptions.optimize_for.default_settings.docx")

    # We can use the OptimizeFor method to ensure optimal compatibility with a specific Microsoft Word version.
    doc.compatibility_options.optimize_for(aw.settings.MsWordVersion.WORD2010)
    print("\nOptimized for Word 2010:")
    ExCompatibilityOptions.print_compatibility_options(options)

    doc.compatibility_options.optimize_for(aw.settings.MsWordVersion.WORD2000)
    print("\nOptimized for Word 2000:")
    ExCompatibilityOptions.print_compatibility_options(options)

@staticmethod
def print_compatibility_options(options: aw.settings.CompatibilityOptions):
    """Groups all flags in a document's compatibility options object by state, then prints each group."""

    for enabled in (True, False):
        print("\tEnabled options:" if enabled else "\tDisabled options:")
        for opt in dir(options):
            if not opt.startswith('__') and not callable(getattr(options, opt)) and getattr(options, opt) == enabled:
                print(f"\t\t{opt}")
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

