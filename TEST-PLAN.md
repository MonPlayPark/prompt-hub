# Prompt Hub V1 — Test Plan

| ID | Scenario | Expected result |
|---|---|---|
| PH-001 | Create/edit prompt | Persists after reload; original creation date retained |
| PH-002 | Favorite/copy/delete prompt | Correct state; exact content copied; deletion confirmed |
| PH-003 | Search/category/tags | Matching results only |
| PH-004 | Template with two variables | Inputs appear and exact variables are replaced |
| PH-005 | Save generated prompt | New prompt appears in library |
| PH-006 | Skill CRUD/search/copy | Markdown retained |
| PH-007 | Export backup | JSON includes schemaVersion and all four stores |
| PH-008 | Import valid backup/merge | IDs in backup overwrite matches; unrelated records remain |
| PH-009 | Import valid backup/replace | Existing stores replaced after confirmation |
| PH-010 | Malformed JSON, duplicate IDs, newer schema | Rejected without changing data |
| PH-011 | Restore on separate device/profile | All records restored |
| PH-012 | Persistent storage request | Reports grant/denial without claiming permanence |
| PH-013 | Responsive UI | No horizontal overflow on Android/desktop |
| PH-014 | Offline after first visit | App shell opens if cached; no sync claim |
| PH-015 | Privacy inspection | No user records/secrets in source repository |
| PH-016 | GitHub Pages subpath | Relative assets and service worker scope work |

Exit criteria: P0 tests pass on Android and desktop; backup/restore on separate profile passes; no data-loss defects remain; owner approves release.
