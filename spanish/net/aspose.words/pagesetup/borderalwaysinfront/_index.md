---
title: PageSetup.BorderAlwaysInFront
second_title: Referencia de API de Aspose.Words para .NET
description: PageSetup propiedad. Especifica dónde se coloca el borde de la página en relación con los textos y objetos que se cruzan.
type: docs
weight: 20
url: /es/net/aspose.words/pagesetup/borderalwaysinfront/
---
## PageSetup.BorderAlwaysInFront property

Especifica dónde se coloca el borde de la página en relación con los textos y objetos que se cruzan.

```csharp
public bool BorderAlwaysInFront { get; set; }
```

### Ejemplos

Muestra cómo crear un borde ancho de banda azul en la parte superior de la primera página.

```csharp
Document doc = new Document();

PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.BorderAlwaysInFront = false;
pageSetup.BorderDistanceFrom = PageBorderDistanceFrom.PageEdge;
pageSetup.BorderAppliesTo = PageBorderAppliesTo.FirstPage;

Border border = pageSetup.Borders[BorderType.Top];
border.LineStyle = LineStyle.Single;
border.LineWidth = 30;
border.Color = Color.Blue;
border.DistanceFromText = 0;

doc.Save(ArtifactsDir + "PageSetup.PageBorderProperties.docx");
```

### Ver también

* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../pagesetup/)
* asamblea [Aspose.Words](../../../)


