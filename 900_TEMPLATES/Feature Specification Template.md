---
tags:
  - dsmc/feature
  - template
status: draft
priority: tbd
effort: tbd
---

# [Feature Name]

## Overview

**Problem Statement:** [What problem does this feature solve?]

**User Value:** [What value does this provide to data stewards?]

**Success Criteria:** [How will we know this feature is successful?]

## User Stories

### Story 1: [Title]
**As a** [type of user]  
**I want** [goal/desire]  
**So that** [benefit/value]

**Acceptance Criteria:**
- [ ] Given [context], when [action], then [expected result]
- [ ] Given [context], when [action], then [expected result]
- [ ] Given [context], when [action], then [expected result]

**Priority:** [High/Medium/Low]  
**Effort:** [S/M/L/XL]

---

### Story 2: [Title]
**As a** [type of user]  
**I want** [goal/desire]  
**So that** [benefit/value]

**Acceptance Criteria:**
- [ ] Given [context], when [action], then [expected result]
- [ ] Given [context], when [action], then [expected result]

**Priority:** [High/Medium/Low]  
**Effort:** [S/M/L/XL]

---

## Technical Specification

### API Endpoints

```
GET    /api/v1/[resource]           # List all
POST   /api/v1/[resource]           # Create new
GET    /api/v1/[resource]/:id       # Get by ID
PUT    /api/v1/[resource]/:id       # Update
DELETE /api/v1/[resource]/:id       # Delete
```

### Data Models

```go
type ResourceName struct {
    ID        string    `json:"id" db:"id"`
    Name      string    `json:"name" db:"name"`
    CreatedAt time.Time `json:"created_at" db:"created_at"`
    UpdatedAt time.Time `json:"updated_at" db:"updated_at"`
}
```

### Database Schema

```sql
CREATE TABLE resource_name (
    id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    name VARCHAR(255) NOT NULL,
    created_at TIMESTAMP DEFAULT NOW(),
    updated_at TIMESTAMP DEFAULT NOW()
);
```

### UI Components

- **Component 1:** [Description]
- **Component 2:** [Description]

## Dependencies

- [ ] [Dependency 1]
- [ ] [Dependency 2]

## Testing Strategy

- **Unit Tests:** [What to test]
- **Integration Tests:** [What to test]
- **E2E Tests:** [User flows to test]

## Open Questions

- [ ] [Question 1]
- [ ] [Question 2]

## Related Features

- [[Feature A]]
- [[Feature B]]
