
# jq Command Reference

This reference section is derived from the official `jq` help documentation and structured for quick lookup of the most commonly used filters and functions for data pipeline manipulation.

## I. Basic Input and Output Filters

These filters handle the data flow and determine the basic structure of the output.

| **Function/Filter**    | **Description**                                                                                        | **Syntax**         | **Example Use Case**                                      |
| ---------------------- | ------------------------------------------------------------------------------------------------------ | ------------------ | --------------------------------------------------------- |
| .(Identity Filter)     | Passes the input data through unchanged. Use this for simple reformatting (e.g., pretty-printing).     | .                  | `echo '{"a": 1}'`                                         |
| .fieldname             | Access the value of a top-level field.                                                                 | .fieldname         | `jq 'session_id'` (Outputs only the session ID value)     |
| .a.b                   | Access a nested value within an object.                                                                | .path.to.field     | `jq '.metadata.subject_id'` (Outputs the subject ID)      |

## II. Transformation and Contruction

These functions are used to change the structure of the data and project new output object.

| **Function/Filter**                 | **Description**                                                             | **Syntax**         | **Example Use Case**                                                   |
| ----------------------------------- | --------------------------------------------------------------------------- | ------------------ | ---------------------------------------------------------------------- |
| {} (Object Construction)            | Creates a new JSON object based on the input data, used for projection.     | {key: .value, ...} | `jq '{id: .session_id}'` (Creates a new object with one key)           |
| [] (Array Construction)             | Creates a JSON array from a stream of inputs.                                   | [...]              | `jq '[session_id]'` (Collects all session IDs into a single array)     |

## III. Conditional Selection (Filtering)

The `select()` function allows you to filter the data stream, similar to a `WHERE` clause in SQL, based on a boolean condition.

| **Function/Filter** | **Description**                                                               | **Syntax**                                                                                      | **Example Use Case**                                               |
| --------------------| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| select(condition)   | Filters input objects, passing only those that satisfy the boolean condition. | `select(.field == "value")`                                                                     | `jq 'select(.status == "FAIL")'` (Isolates all failed log entries) |
| **                  | `(Piping)**`                                                                  | Chains filters together, sending the output of the left filter as the input to the right filter | `filterA`                                                            |

You now have everything needed to complete the detailed plan and the template files to organize your work. Your next action is to open `docs/jq-utility/getting-started.md` and start running those commands in your terminal to fill in the outputs!

Good luck!