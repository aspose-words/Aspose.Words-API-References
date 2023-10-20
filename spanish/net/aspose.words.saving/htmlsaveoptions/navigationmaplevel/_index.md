---
title: HtmlSaveOptions.NavigationMapLevel
linktitle: NavigationMapLevel
articleTitle: NavigationMapLevel
second_title: Aspose.Words para .NET
description: HtmlSaveOptions NavigationMapLevel propiedad. Especifica el nivel máximo de encabezados completados en el mapa de navegación al exportar a formatos EPUB MOBI o AZW3 . El valor predeterminado es3  en C#.
type: docs
weight: 390
url: /es/net/aspose.words.saving/htmlsaveoptions/navigationmaplevel/
---
## HtmlSaveOptions.NavigationMapLevel property

Especifica el nivel máximo de encabezados completados en el mapa de navegación al exportar a formatos EPUB, MOBI o AZW3 . El valor predeterminado es`3` .

```csharp
public int NavigationMapLevel { get; set; }
```

## Observaciones

El mapa de navegación permite a los agentes de usuario proporcionar una manera fácil de navegar a través de la estructura del documento. Generalmente los puntos de navegación corresponden a los encabezados del documento. Para completar encabezados hasta el nivel**norte** asigna este valor a`NavigationMapLevel`.

De forma predeterminada, se completan tres niveles de títulos: párrafos de estilos**Título 1** ,**Título 2** y**Título 3**. Puede establecer esta propiedad en un valor de 1 a 9 para solicitar el nivel máximo correspondiente. Establecerla en cero reducirá el mapa de navegación a solo la raíz del documento o las raíces de las partes del documento.

### Ver también

* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
