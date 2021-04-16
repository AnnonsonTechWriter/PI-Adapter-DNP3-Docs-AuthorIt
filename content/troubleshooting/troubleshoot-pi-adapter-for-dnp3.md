---
uid: TroubleshootPIAdapterForDNP3
---

# Troubleshoot PI Adapter for DNP3

PI Adapter for DNP3 provides troubleshooting features that enable you to verify adapter configuration, confirm connectivity, and view message logs. If you are unable to resolve issues with the adapter or need additional guidance, contact OSIsoft Technical Support through the [OSIsoft Customer Portal](https://my.osisoft.com/).

## Check configurations

Incorrect configurations can interrupt data flow and cause errors in values and ranges. Perform the following steps to confirm correct configuration for your adapter.

1. Navigate to [data source configuration](xref:PIAdapterForDNP3DataSourceConfiguration) and verify that <!-- Insert data source parameters that need to be checked --> are correct.
2. Navigate to [data selection configuration](xref:PIAdapterForDNP3DataSelectionConfiguration) and verify the following for each configured data selection item below:

    <!-- Insert data selection parameters that need to be checked-->

3. Navigate to [egress endpoints configuration](xref:EgressEndpointsConfiguration) and verify each configured endpoint's **Endpoint** property and credentials are correct.

    * For a PI server or EDS endpoint, verify **UserName** and **Password**.
    * For an OCS endpoint, verify **ClientId** and **ClientSecret**.

## Check connectivity

Perform the following steps to verify active connections to the data source and egress endpoints.

1. Start PI Web API and verify that the PI point values are updating or start OCS and verify that the stream values are updating.
2. If configured, use a health endpoint to determine the status of the adapter.<br>For more information, see [Health and diagnostics](xref:HealthAndDiagnostics).

## Check logs

Perform the following steps to view the adapter and endpoint logs to isolate issues for resolution.

1. Navigate to the logs directory:<br>
    Windows: `%ProgramData%\OSIsoft\Adapters\DNP3\Logs`<br>
    Linux: `/usr/share/OSIsoft/Adapters/DNP3/Logs`.
2. Optional: Change the log level of the adapter to receive more information and context.<br>For more information, see [Logging configuration](xref:LoggingConfiguration).
