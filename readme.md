### Commands:

- `npm start` &mdash; Starts the server in production mode.
- `npm run start:dev` &mdash; Starts the server in development mode.
- `npm run lint` &mdash; Runs ESLint code checks.
- `npm lint:fix` &mdash; The same as above, but also automatically corrects simple errors.

### Paths:

GET:
- `{{baseUrl}}/contacts` &mdash; Get all user contacts | Required: token
- `{{baseUrl}}/contacts?page=1&limit=20` &mdash; Get user contacts, page 1, 20 per page | Required: token
- `{{baseUrl}}/contacts?favorite=true` &mdash; Get all favotire user contacts | Required: token
- `{{baseUrl}}/contacts/:id` &mdash; Get contact by Id | Required: token
- `{{baseUrl}}/users/logout` &mdash; Log out | Required: token
- `{{baseUrl}}/users/current` &mdash; Get current user | Required: token
- `{{baseUrl}}/users/verify/:verificationToken` &mdash; Set the user as verified

POST:
- `{{baseUrl}}/contacts` &mdash; Add contact | Required: name, email and phone, token
- `{{baseUrl}}/users/signup` &mdash; Sign up user | Required: email, password
- `{{baseUrl}}/users/login` &mdash; Log in | Required: email, password
- `{{baseUrl}}/users/verify` &mdash; Resend verification email | Required: email

PUT:
- `{{baseUrl}}/contacts/:id` &mdash; Update contact | Required: name, email or phone, token

PATCH:
- `{{baseUrl}}/contacts/:id/favorite` &mdash; Set contact as favorite | Required: favorite (true/false), token
- `{{baseUrl}}/users` &mdash; Update subscription | Required: subscription ("starter", "pro" or "business"), token
- `{{baseUrl}}/users/avatars` &mdash; Set a new avatar for the user | Required: avatar (img file), token

DELETE:
- `{{baseUrl}}/contacts/:id` &mdash; Delete contact | Required: token
