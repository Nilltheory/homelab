# Ledgerdesk deployment

I used the Debian homelab to host a prototype of Ledgerdesk, a tool for tracking client work in a chartered accountant's office. I built the frontend on Windows, copied the build with SCP, and served it through Nginx in Docker. Tailscale Serve made the prototype available over private HTTPS.

During deployment I encountered a 403 and then a blank page. The browser expected JavaScript but received the HTML fallback instead. I checked the Nginx logs, confirmed that the build asset existed, and worked through permissions and asset serving until the frontend rendered.

I installed PostgreSQL and separately tested a read-only work-files API using a schema migration and sample data. The endpoint returned successfully after I corrected the database authentication settings. The hosted frontend prototype still uses in-memory sample records.

## To document

- Current deployment and update steps
- Database backup and restore testing
