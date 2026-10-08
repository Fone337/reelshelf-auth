# ReelShelf sign-in relay

Served by GitHub Pages at https://auth.commandz.co.uk. Google's OAuth redirect for ReelShelf Connect points at
`https://auth.commandz.co.uk/callback/`; the page forwards `code`, `state` and `error` to
`https://reelhouse.commandz.co.uk/oauth/callback`. It exists because Bluehost's ModSecurity rejects Google's
callback (it adds `iss=https://accounts.google.com`), and ModSecurity can't be turned off on that hosting.
