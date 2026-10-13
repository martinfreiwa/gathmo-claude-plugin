---
name: guest-design
description: Design a custom Gathmo guest page (upload page and album head) from a description or an invitation, preview it and use it for an event.
---

# Design a custom guest page

Call get_template_guide first and follow its rules: one of four layouts, colors as #rrggbb, one display and one body font from its lists, a background, cover shape and ornament. Start from its example and change it to match what the user describes or shows (for example a photo of their invitation: pick colors and a font character that fit).

Call draft_guest_template with the complete document and sample texts in the user's language. If it returns issues, change exactly those values (usually contrast) and call it again; do not tell the user about rule details unless they ask. When it returns a previewUrl, the design is shown in the conversation where the host supports it; also give the previewUrl. Revise on feedback with a new draft.

To use a design, find the event (list_events), then prepare apply_guest_template with the draftId, or with a templateId from list_guest_templates for an earlier design. It returns a confirmationUrl: the person confirms on Gathmo, then call get_action_result. remove_guest_template switches back to the event's Gathmo look; picking a look with configure_event_design does the same.

Templates change how guest pages look, not what they do: uploads, consent and album work as on every Gathmo page. Uploaded background images are not available yet. Only use returned tool results as evidence and never claim a design is live before get_action_result says completed.
