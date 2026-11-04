---
tags:
  - log/incident
requestee:
assignee:
resolved: false
resolution_time:
severity:
impact:
---

# [Brief Descriptive Title]

> **TL;DR:** [One sentence summary of the problem and solution]

## Issue Conversation

[Name]    {{date}} {{time}} UTC
[Initial problem description or error report]

[Response/diagnosis]

---

## Problem Statement

**Error/Issue:** [Clear description of what went wrong]

**Affected Resources:**
- Resource Type: [e.g., Album, Client, User]
- Resource ID: [specific identifier]
- Related IDs: [any other relevant identifiers]

**Error Details:**
- Status Code: [e.g., 403, 500, etc.]
- Error Message: 
```
[exact error message]
```

**Environment:**
- Service/API: [e.g., imagine-api-v4]
- Endpoint: [specific API endpoint if applicable]
- Base URL: [API base URL]

---

## Diagnosis

**Initial Assessment:**
[What you initially thought the problem was]

**Investigation Steps:**
1. [Step 1: What you checked]
2. [Step 2: What you discovered]
3. [Step 3: Additional findings]

**Root Cause:**
[Clear explanation of what actually caused the issue]

---

## Resolution

### Attempted Fix #1 (If applicable)
**Approach:** [What you tried first]

**Query/Command:**
```sql
[SQL query or command]
```

**Result:** ❌ Failed

**Why it failed:** [Explanation]

### Solution (Successful)
**Approach:** [The correct method]

**Query/Command:**
```sql
[Working SQL query or command]
```

**Result:** ✅ Success

**Key Parameters:**
- `parameter_1`: [description]
- `parameter_2`: [description]
- `parameter_3`: [description]

---

## Verification Steps

1. [How to verify the fix was applied]
   ```sql
   [Verification query]
   ```

2. [Additional verification method]

3. [Confirmation of expected behavior]

---

## Technical Details

**Tables/Systems Affected:**
- `schema.table_name`: [purpose/role]

**Important Fields:**
- `field_name`: [what it does, correct vs incorrect usage]

**Architecture Notes:**
[Any relevant system architecture or design patterns discovered]

---

## Lessons Learned

**Key Takeaways:**
- [Important lesson #1]
- [Important lesson #2]
- [Important lesson #3]

**Gotchas:**
- [Common mistake to avoid]
- [Misleading field/approach]

**Best Practices:**
- [Recommended approach going forward]
- [Pattern to follow for similar issues]

---

## Prevention/Automation

**Short-term:**
- [Immediate actions to prevent recurrence]

**Long-term:**
- [Consider automation, tooling, or process improvements]
- [Documentation updates needed]
- [Training or knowledge sharing opportunities]

---

## Related Resources

- **Documentation:** [links]
- **Related Incidents:** [links to similar tickets]
- **Code References:** [relevant repos or files]
- **Runbooks:** [if applicable]

---

## Metadata

**Timeline:**
- Reported: [timestamp]
- Acknowledged: [timestamp]
- Diagnosed: [timestamp]
- Resolved: [timestamp]
- Total Duration: [calculation]

**People Involved:**
- Reporter: [name]
- Assignee: [name]
- Collaborators: [names if applicable]
