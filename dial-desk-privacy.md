# Lumacode Dial Desk Privacy Notice

Last updated: 9 November 2026

Lumacode operates Dial Desk, a sales calling and booking tool. This notice explains the Google Calendar connection and related booking information. For questions or requests, contact info@lumacode.io.

## Google Calendar access

If an authorised user connects Google Calendar, Dial Desk requests the Google Calendar events permission. This permission permits viewing and editing events across calendars accessible to the Google account. Dial Desk uses the connection to create, update and delete events for its own booked setup calls in the account's primary calendar; its current implementation does not list or read existing unrelated events. The app can work in the background using an OAuth refresh token.

A Dial Desk event can include the clinic's business name, contact name, telephone number, invite email if present, booking notes, time, a link to Dial Desk and an internal lead identifier. These details may relate to people other than the Google account holder. Google receives this information to provide the calendar service. Separate email invitations may be sent through Resend using booking details supplied to Dial Desk.

## Storage and access

Dial Desk runs on Cloudflare and stores its Google refresh token and event identifiers and links in a Cloudflare D1 database. The Google access token is kept in server memory. Signed-in Dial Desk users can see the connection status and event links and can initiate a sync or disconnect the integration. The app's Google OAuth client credentials are stored as Cloudflare Worker secrets.

Google Calendar data obtained through this integration is used for the calendar functionality described above. Dial Desk does not pass Google Calendar API data to its AI, email or calling providers. Other lead data and call transcripts are handled separately by the relevant calling, email and AI functions.

## Retention and disconnection

The refresh token is stored until the integration is disconnected. Event identifiers and links are retained without a set automatic expiry; they are removed when the corresponding booking is removed while the integration is connected. Disconnecting in Dial Desk deletes its stored refresh-token record and attempts to revoke access with Google, but does not delete existing calendar events or the saved event links. You can also revoke access through your Google Account's third-party connections. To request access, correction or deletion of information, contact info@lumacode.io. Existing events may also be removed directly in Google Calendar.

## Questions and changes

Contact info@lumacode.io with privacy questions or requests. Depending on your location, applicable law may give you rights concerning your information. This notice may be updated as the service changes; the date above will be revised when it is updated.
