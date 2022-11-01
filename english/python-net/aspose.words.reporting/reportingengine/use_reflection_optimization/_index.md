---
title: use_reflection_optimization property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets a value indicating whether invocations of custom type members performed via reflection API are  optimized using dynamic class generation or not"
type: docs
weight: 40
url: /python-net/aspose.words.reporting/reportingengine/use_reflection_optimization/
---

## ReportingEngine.use_reflection_optimization property

Gets or sets a value indicating whether invocations of custom type members performed via reflection API are 
optimized using dynamic class generation or not. The default value is ``True``.


There are some scenarios where it is preferrable to disable this optimization. For example, if you are dealing 
with small collections of data items all the time, then an overhead of dynamic class generation can be more 
noticeable than an overhead of direct reflection API calls.

The option does not have effect when run on iOS and reflection optimization is not used.


### See Also

* module [aspose.words.reporting](../../)
* class [ReportingEngine](../)

