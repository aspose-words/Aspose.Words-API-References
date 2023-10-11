---
title: ReportingEngine.UseReflectionOptimization
second_title: Referencia de API de Aspose.Words para .NET
description: ReportingEngine propiedad. Obtiene o establece un valor que indica si las invocaciones de miembros de tipo personalizado realizadas a través de la API de reflexión están optimizadas mediante la generación dinámica de clases o no. El valor predeterminado esverdadero .
type: docs
weight: 70
url: /es/net/aspose.words.reporting/reportingengine/usereflectionoptimization/
---
## ReportingEngine.UseReflectionOptimization property

Obtiene o establece un valor que indica si las invocaciones de miembros de tipo personalizado realizadas a través de la API de reflexión están optimizadas mediante la generación dinámica de clases o no. El valor predeterminado es`verdadero` .

```csharp
public static bool UseReflectionOptimization { get; set; }
```

### Observaciones

Hay algunos escenarios en los que es preferible desactivar esta optimización. Por ejemplo, si está tratando con pequeñas colecciones de elementos de datos todo el tiempo, entonces una sobrecarga de generación de clases dinámicas puede ser más notable que una sobrecarga de llamadas API de reflexión directa. La opción no tiene efecto cuando se ejecuta en No se utiliza iOS ni la optimización de la reflexión.

### Ver también

* class [ReportingEngine](../)
* espacio de nombres [Aspose.Words.Reporting](../../reportingengine/)
* asamblea [Aspose.Words](../../../)


