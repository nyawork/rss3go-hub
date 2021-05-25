# RSS 3 Go Hub

> You are the hub, of all you have, of all you love.
> Keep going.

## About

We've split the RSS3 types into a new repo [rss3go_lib](https://github.com/nyawork/rss3go_lib)

It's still in early develop stage, and those it cannot run correctly / functionally. Hope we can finally make it.

Check [RSS3-Hub](https://github.com/NaturalSelectionLabs/RSS3-Hub/) and [RSS3](https://rss3.io/) for more information.

## Auth

We are using similar methods for signature authentication in [go-eth-crypto-test](https://github.com/nyawork/go-eth-crypto-test)

They should be already deployed in rss3go_lib .

## Endpoints

### Files

- GET `/files/:fid` - get a file
  
  Request body: Null

- POST `/files` - upload a new file (Signature within)

  Request body: Full file object (Should be new)

- PUT `/files` - change a file (Signature within)

  Request body: Full file object (Should already exist)

- DELETE `/files` - delete a file (Signature within)

  Request body: (Your hexadecimal signature of string "delete")

    ``` json
    {
        "signature": "xxxxxx00" // Should end with 00 or 01
    }
    ```
