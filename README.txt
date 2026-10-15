Touchigh Social prototype (self-hostable, protected copy)

Sign-in
- Open index.html and sign in with an allowed @touchigh.ai email and the team password.
- The app and every file in ws/ are encrypted. They only open in the browser after a correct sign-in,
  so the folder is safe to put on any static host.
- Host it over https (or open it straight from disk). Browsers only allow the decryption over a secure connection.

Optional server-side Basic Auth (Apache)
- server-auth/.htaccess and server-auth/.htpasswd hold one login per allowed email with the same team password (bcrypt hashes).
- Put .htpasswd outside the web root, set its absolute path in .htaccess, and copy .htaccess next to index.html.
- nginx: use the same file with  auth_basic "Touchigh Social";  auth_basic_user_file /path/to/.htpasswd;
- With Basic Auth on, link previews (Slack, LinkedIn, X) can't fetch the page, so shared links won't show a card.

Social preview and robots
- og:image and twitter:image are relative paths. Facebook, LinkedIn and X need a full URL: ask for a rebuild with your address.
- robots.txt and the robots meta tag keep search engines and AI crawlers out. robots.txt only works at the root of a domain.
