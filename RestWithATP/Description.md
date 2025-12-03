## Description of this Intergation

This Integration is designed with a REST Adapter in Trigger mode with Single Parameter as Country ID(Ex: 52781). After passing the parameter into the integration it will take the corresponding 2-Digit ISO Code for that country from ATP Database. So the ATP End Point has been configured as Invoke Connection. Lastly using the that retrieved two digit code it will invoke Readily avialable REST End Point over Internet with Address:
`https://restcountries.com/v3.1/alpha/IN`, which is eventually return Country Information from that Country Id.

## What is the difference between Schedule Parameter, Global variable and Integration Properties?

| Feature       | Schedule Parameters                                                                                            | Global Variables                                                                                   | Integration Properties                                                                                                                     |
|---------------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Primary Use   | Pass values to a specific run of a scheduled integration and persist state between runs                        | Store and share data within a single integration flow's runtime instance                           | Externalize configuration settings that might change across environments (e.g., email addresses, file paths)                               |
| Scope         | Available across all runs of a scheduled integration (value persists after a run completes)                    | Available throughout the entire lifecycle of a single integration flow execution                   | System-wide (defined at the integration level, but can be overridden at runtime or across environments)                                    |
| Mutability    | Can be read and updated within the integration flow during execution                                           | Can be read and updated throughout the integration flow                                            | Read-only within the integration flow, but their values can be overridden from the OIC Console at runtime without editing the integration  |
| Data Types    | Primarily simple types (string, date, number, boolean) and limited to 256 characters (for tracking batch data) | Can be simple types or complex types (e.g., object types from an integration's trigger or invokes) | Primarily simple string key-value pairs for configuration data                                                                             |
| Configuration | Defined within the schedule configuration panel of a scheduled integration                                     | Defined using the "Assign" action or variables panel within the integration canvas                 | Defined in the integration's properties and managed in the OIC Console's properties management section                                     |


## How to create NXSD File to read structured data into XML Format?

Please refer Oracle Documentation: [Oracle NXSD](https://docs.oracle.com/cd/E23943_01/integration.1111/e10231/nfb.htm#CCHCIGCA)


## Data Mapping

There are basically three cases a mapper appear in the flow.

<img src="./images/Mapper1.png" alt="OIC Mapper" >

## How to conditionally map a target Node? Like if an expression return true then only the mapping should happen or else no mapping.

If XSL Construct

<img src="./images/Cond_mapping.png" alt="Conditional Mapping" >
