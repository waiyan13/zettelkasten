# OOPS Writeups

:technical_writing:

## Structure

- Title
  - The tile with the same suffix 'How we got there'
  - The name of the document is the description of the incident
- Executive summary
  - This section is usually about
    - When it happened
    - The impact
    - Explanation of the failure mode
    - Difficult aspects of the incident
- Background
  - Technical details surrounding the incident
- Narrative description
  - Prologue
    - Key info about implementation decisions and changes
    - Include timeline info as subsections
  - The trigger
    - Acts as crucial turning point in the incident
    - Describe how the system reached the state of customer impact
  - Impact
    - From the start of the trigger to return to normal state
    - Include timestamps as well, from the start of the impact
  - Epilogue
    - List the work done to fix the incident
- Contributors/enablers
  - Things that attribute to the causing of incident
  - One subsection for each enabler
- Mitigators
  - Which part of the system help reduce the blast radius of the incident
- Risks
  - Items with technical or people related that induce danger in system
  - Did the incident create new risks or supplement existing known risks?
  - Combine contributors to see higher level patterns as risks
  - Avoid hindsight bias
- Challenges in handling
  - Hightlight key obstructions during handling the incident

## Reference

[OOPS Writeups](https://surfingcomplexity.blog/2021/11/21/oops-writeups/)


