# GetLensBidsIgnored

## API

<table><thead><tr><th width="171">API</th><th>/v1/get_lens_bids_ignored</th></tr></thead><tbody><tr><td>Title</td><td>GetLensBidsIgnored</td></tr><tr><td>Description</td><td>Get the bids which ignored by the curator.</td></tr><tr><td>Authorization</td><td>Not required</td></tr><tr><td>Method</td><td><code>POST</code></td></tr></tbody></table>

## Request Parameters

<table><thead><tr><th width="177">Name</th><th width="105">Type</th><th width="133">Required</th><th>Description</th></tr></thead><tbody><tr><td>profileIds</td><td>int[]</td><td>YES</td><td>The Lens profile id list of the curators</td></tr></tbody></table>

## Parameter Content Type

application/json

## Request and Response Example

### Request

#### cURL Code

```bash
curl -X 'POST' \
  'https://api.takoyaki.so/v1/get_lens_bids_ignored' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "profileIds": [
    36113
  ]
}'
```

#### Request URL

`https://api.takoyaki.so/v1/get_lens_bids_ignored`

### Response

```json
{
  "status": "success",
  "data": {
    "bids": [
      {
        "id": 18729,
        "index": 70,
        "platform_type": "polygon",
        "content_uri": "",
        "bid_token": "0x0000000000000000000000000000000000000000",
        "bid_address": "0xCe41cdCCA1849CaD58DaACc6005B1990Be04e1F0",
        "bid_amount": 1000000000000,
        "bid_expires": 1691012582,
        "to_profiles": [
          36113
        ],
        "curator_profile_id": 0,
        "curator_pub_id": "0x00",
        "state": "Pending",
        "bid_type": "Mirror",
        "block_number": 0,
        "others": {
          "pubIdPointed": 2,
          "profileIdPointed": 36112
        },
        "events": {
          "addBidEvent": {
            "state": "Pending",
            "tx_hash": "0xfef79bb3082eed54df52319cac60563bd7430d4c165f9927bcd362d33862e9f7",
            "event_name": "addBidEvent",
            "block_number": 38553832,
            "block_timestamp": 1690969382
          }
        },
        "create_at": 1690969382,
        "update_at": 1690969382,
        "is_ignored": false
      }
    ],
    "total": 1
  }
}
```
