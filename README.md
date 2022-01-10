# workbook-cover

[![GitHub issues](https://img.shields.io/github/issues/iu-actions/workbook-cover)](https://github.com/iu-actions/workbook-cover/issues)

This action generates the cover page for an IU workbook.

## Found a bug? 💁‍♀️

Thanks for letting us know! Please [file an issue](../../issues/new?assignees=&labels=&template=bug_report.md&title=) and we should reply shortly.

## Configuration

This action requires the presence of inputs, which are listed below.

### Inputs
- `first_name`: The first name of the student. (**required**)
- `last_name`: The last name of the student. (**required**)
- `email`: The email of the student. (**required**)
- `id`: The id of the student. (**required**)
- `degree`: The degree pursued by the student. (**required**)
- `semester`: The current semester of the student. (**required**)
- `address`: The address of the student. (**required**)

- `course_name`: The name of the course. (**required**)
- `course_id`: The id/number of the course. (**required**)
- `professor`: The professor of the course. (**required**)
- `tutor`: The tutor of the course. (**required**)

*Note*: The following files must be present at the specified location and contain the appropriate variables.

- `format_doc`: Path to the Microsoft Word template of the cover page. (**required**) → [Learn more](https://pandoc.org/MANUAL.html#option--reference-doc)
- `template_doc`: Path to the Markdown template of the cover page to define the structure. (**required**) → [Learn more](https://pandoc.org/MANUAL.html#option--template)

## Example

Below you will find an example of how you can use this action.

```yaml
uses: iu-actions/workbook-cover@v2
with:
  # student details
  id: 12345678
  first_name: John
  last_name: Doe
  email: john.doe@example.edu
  degree: B. Sc. Computer Science
  semester: 2. Semester
  
  # address details
  address: | 
    MIT Room 2-245
    Department of Mathematics
    Cambridge MA 02139
          
  # course details
  course_name: Linear Algebra I
  course_id: LA101
  professor: Prof. Dr. Gilbert Strang
  tutor: Jane Doe
          
  # configuration details
  format_doc: .iu/workbook/cover/format.docx
  template_doc: .iu/workbook/cover/template.md
  ```
