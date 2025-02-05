---
title: Correlate Logs and Tests
kind: documentation
description: Correlate your logs with your test traces.
further_reading:
  - link: "/tests"
    tag: "Documentation"
    text: "Learn about Test Visibility"
---

{{< site-region region="gov" >}}
<div class="alert alert-warning">Test Visibility is not available in the selected site ({{< region-param key="dd_site_name" >}}) at this time.</div>
{{< /site-region >}}

## Overview

You can correlate Test Visibility data with [logs injected into Datadog][1], which allows you to view and analyze logs for specific test cases.

{{< img src="continuous_integration/correlate_logs_and_tests.png" 
  alt="Examine logs for specific test cases with logs and tests correlation." style="width:90%" >}}

## Setup

Correlation can be configured differently depending on how you [send your tests data to Datadog][2].

{{< tabs >}}
{{% tab "Cloud CI provider (agentless)" %}}

Agentless log submission is supported for the following languages and frameworks:

- Java with `dd-trace-java >= 1.35.2` and Log4j2.

Use the following environment variables to enable and configure agentless log submission:

| Name | Description | Default value |
|---|---|---|
| `DD_AGENTLESS_LOG_SUBMISSION_ENABLED` (required) | Enables/disables log submission | `false` 
| `DD_AGENTLESS_LOG_SUBMISSION_LEVEL` (optional) | Sets log level for agentless submission | `INFO`
| `DD_AGENTLESS_LOG_SUBMISSION_QUEUE_SIZE` (optional) | Sets the maximum size of pending logs queue | `1024`
| `DD_AGENTLESS_LOG_SUBMISSION_URL` (optional) | Sets custom URL for submitting logs | -

{{% /tab %}}
{{% tab "On-Premises CI provider (Datadog Agent)" %}}

1. [Set up log collection][1] through the Datadog Agent.
2. Follow the steps described in [Correlate Logs and Traces][2].

[1]: /logs/log_collection/
[2]: /tracing/other_telemetry/connect_logs_and_traces/

{{% /tab %}}
{{< /tabs >}}

## Further Reading

{{< partial name="whats-next/whats-next.html" >}}

[1]: /logs/log_collection/
[2]: /tests/setup/
[3]: /tracing/other_telemetry/connect_logs_and_traces/
