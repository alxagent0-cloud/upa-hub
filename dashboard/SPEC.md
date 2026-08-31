Build a single-file web app at dashboard/index.html for "UPA Hub" - a personal assistant dashboard. Requirements:

DESIGN: Dark modern theme (background #0d1117, cards #161b22, accent #58a6ff), fully mobile-responsive (primary target: phone), clean sans-serif font. No frameworks - pure HTML/CSS/JS in ONE file, no external dependencies, must work offline from file://.

DATA MODEL: Three linked entities stored in localStorage key "upa_data": people[] {id, name, role/company, phone, email, notes, tags[], meetings:[meetingIds], documents:[docIds]}, meetings[] {id, title, datetime, personId, location, agenda/topics, status(upcoming/completed), documents:[docIds], notes}, documents[] {id, name, type(pdf/doc/sheet/note/link), urlOrPath, personId?, meetingId?, addedDate}.

FEATURES:
1) Bottom tab bar (phone-style): Contacts | Meetings | Documents | Dashboard.
2) Contacts tab: searchable card list; tapping a card opens detail view showing ALL their info, their meetings list, and their documents library.
3) Meetings tab: chronological list grouped Upcoming/Past, each showing linked person and topic; tap for detail with agenda + documents.
4) Documents tab: full library, filterable by type and by person.
5) Dashboard tab: stats overview (counts), next upcoming meeting highlighted, recently added items.
6) Floating + button on each tab to add new entries with proper forms.
7) Global search across everything.
8) Data persists in localStorage; Settings gear with Export JSON (download file) and Import JSON (file picker).
9) Seed with ONE realistic example: person Alex Morgan (Business Consultant), meeting Wednesday Aug 26 2026 14:00 about Q4 partnership proposal, one draft document linked to both.

QUALITY: All interactive features must actually work (forms save, lists update, detail views navigate back). Empty states with helpful text. Print the final file size at the end.
