# Gathmo

Gathmo is an event album for photos, videos and voice messages. Guests scan a QR code and upload from their phone, without an app or account. This plugin lets Claude help hosts, planners and businesses run their Gathmo events.

## Install

In Claude Code:

```
/plugin install gathmo --marketplace martinfreiwa/gathmo-claude-plugin
```

In Claude, add Gathmo from the connector directory, or add a custom connector with `https://api.gathmo.com/mcp/gathmo-claude`.

## What you can do

- Plan photo, video and voice collection for a wedding, birthday, party or business event, and draft wording for invitations, reminders and thank-you notes. This works without a Gathmo account.
- Create an event or change its name, date, language, media options and guest-page design.
- Get the guest link and downloadable QR files, and prepare printable QR signs (A4, A6 or A7; the printed sign text is currently in English).
- Choose live photo wall settings such as display mode, pacing, background and QR visibility. Starting the wall on a screen stays in your Gathmo dashboard.
- Check contribution counts and album metadata, choose a cover photo, and prepare an album download within the download rights your plan already has.
- Apply an existing workspace brand to a business event.
- Design your own guest page: describe it (or show your invitation), see a live preview right in the conversation, and use it for your event's upload page and album. Picking a Gathmo look switches back at any time.
- Connect a photo booth: set up an event-specific connection, prepare a local uploader, and check whether a test photo reached the album.

## Every change is confirmed on Gathmo

Claude cannot change your events by itself. Creating or changing an event, preparing QR files or downloads, and connecting a booth each open a Gathmo confirmation page in your browser. Nothing happens until you confirm it there while signed in. Read-only members of a workspace cannot make changes, and the plugin never buys a plan, deletes an event or sends emails or messages to your guests.

## What data is shared

The plugin connects Claude to Gathmo's server at https://api.gathmo.com/mcp/gathmo-claude. You sign in to Gathmo in your browser and approve the connection there; Claude never sees your Gathmo password.

- Claude sends Gathmo the details of each request, such as an event name, date, language, design or wall settings, welcome text or the ID of a selected photo.
- Gathmo returns only what your account is allowed to see: event settings, guest links, contribution counts, and album metadata such as media type, status, file size, duration and upload time.
- Guest photos, videos and voice recordings are not sent to Claude. Guest names, transcripts and private media are left out. QR files and album downloads open as links on Gathmo that only your account can use, and they expire within 15 minutes.
- The optional booth uploader is a separate program that the booth operator downloads from Gathmo and runs on the booth computer. It uploads finished booth photos from one chosen folder directly to Gathmo for that event. Claude does not see those files or the uploader's setup key. A connected booth keeps uploading for up to 120 days, also after you sign out, until you stop it, replace its setup file or disconnect.

## Disconnect

Ask Claude for your Gathmo connection settings and confirm the disconnect on the Gathmo page that opens. Signing out of Gathmo in the browser you used to connect also ends the connection. You can remove the Gathmo connector from Claude's settings at any time.

## Links

- How it works, example prompts and troubleshooting: https://gathmo.com/ai-assistants.html
- Help and support: https://gathmo.com/help or hello@gathmo.com
- Privacy notice for this integration: https://gathmo.com/ai-assistants-privacy.html
- Terms of service: https://gathmo.com/terms

Gathmo is not affiliated with Anthropic or with any photo-booth software vendor. Booth software named in this plugin is mentioned only to describe compatibility.
