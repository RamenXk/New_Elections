# Client Side

## Summary
Build the frontend views, user interface, and API integration for election participation, dashboards, and history.

## Responsibilities
- Build navigation and global UI elements
  - Permanent navigation bar containing BDPA logo and app title
  - Display summary counts for:
    - total elections
    - open elections
    - closed elections
- Build dashboard view
  - Role-specific dashboard for voters, moderators, administrators, reporters
  - Show upcoming elections and deadlines
  - Show notifications for elections that are about to close
- Build election view
  - Show election details and options
  - Enable eligible voters to submit or update votes for open elections
  - Display closed election results in a clear, accessible format
  - Highlight the winner and eliminated options
  - Mark the current user’s first choice prominently if they voted
- Build history view
  - Show past elections and result summaries
  - Support owned vs unowned election display as needed
- Build user management UI for admins
  - Create/update/delete non-administrator users
  - Assign/remove voters and moderators from elections
- Integrate with backend APIs
  - Use API contract from Server Side One for auth, election data, user management
  - Use Server Side Two endpoints for vote submission and results data
  - Handle errors, loading states, and role-based rendering
- Maintain UI quality
  - Responsive layout
  - Accessible labels and status messages
  - Clearly separate read-only and editable states

## Notes
- Start frontend work with mocked API responses if backend endpoints are not yet available
- Keep the frontend branch isolated to UI files/components and API integration code only
