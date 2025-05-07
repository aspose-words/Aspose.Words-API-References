---
title: VbaReference.type property
linktitle: type property
articleTitle: type property
second_title: Aspose.Words for Node.js
description: "VbaReference.type property. Gets [VbaReferenceType](../../vbareferencetype/) object that indicates the type of reference that a [VbaReference](../) object represents."
type: docs
weight: 20
url: /nodejs-net/aspose.words.vba/vbareference/type/
---

## VbaReference.type property

Gets [VbaReferenceType](../../vbareferencetype/) object that indicates the type of reference that a [VbaReference](../) object represents.



```js
get type(): Aspose.Words.Vba.VbaReferenceType
```

### Examples

Shows how to get/remove an element from the VBA reference collection.

```js
test('RemoveVbaReference', () => {
  const brokenPath = "X:\\broken.dll";
  let doc = new aw.Document(base.myDir + "VBA project.docm");

  let references = doc.vbaProject.references;
  expect(references.count).toEqual(5);

  for (let i = references.count - 1; i >= 0; i--)
  {
    let reference = doc.vbaProject.references.at(i);
    let path = getLibIdPath(reference);

    if (path == brokenPath)
      references.removeAt(i);
  }
  expect(references.count).toEqual(4);

  references.remove(references.at(1));
  expect(references.count).toEqual(3);

  doc.save(base.artifactsDir + "VbaProject.RemoveVbaReference.docm"); 
});


/// <summary>
/// Returns string representing LibId path of a specified reference. 
/// </summary>
function getLibIdPath(reference)
{
  switch (reference.type)
  {
    case aw.Vba.VbaReferenceType.Registered:
    case aw.Vba.VbaReferenceType.Original:
    case aw.Vba.VbaReferenceType.Control:
      return getLibIdReferencePath(reference.libId);
    case aw.Vba.VbaReferenceType.Project:
      return getLibIdProjectPath(reference.libId);
    default:
      throw new Error("Unknown reference type.");
  }
}

/// <summary>
/// Returns path from a specified identifier of an Automation type library.
/// </summary>
function getLibIdReferencePath(libIdReference)
{
  if (libIdReference != null)
  {
    let refParts = libIdReference.split('#');
    if (refParts.length > 3)
      return refParts.at(3);
  }

  return "";
}

/// <summary>
/// Returns path from a specified identifier of an Automation type library.
/// </summary>
function getLibIdProjectPath(libIdProject)
{
  return libIdProject != null ? libIdProject.substring(3) : "";
}
```

### See Also

* module [Aspose.Words.Vba](../../)
* class [VbaReference](../)

