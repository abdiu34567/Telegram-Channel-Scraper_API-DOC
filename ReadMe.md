# ⚡️ TELEGRAM CHANNEL SCRAPER ⚡️

> [Updated Version Of Fana Protocol](https://github.com/baydisng13/fana-doc/blob/main/README.md)

> Base Url : https://fanatgchannelscraper.herokuapp.com/api/

<br>

## End-Points:

- ⚡️`get_info/{channel_username}`
- ⚡️`get_post/{channel_username}`
- ⚡️`channel_value/{channel_username}`
- ⚡️`getlastpost_id/{channel_username}`
- ⚡️`getpostby_id/{channel_username}/{post_id}`
- ⚡️`getmultiplechannels_post/${channel_username}`

<br>

### Error Message: `(For All End-Points)`

| Error-Message                                       | Description                             |
| --------------------------------------------------- | --------------------------------------- |
| NO_VALID_CHANNEL_USERNAME_FOUND                     | invalid channel username                |
| ONLY_CHANNELS_ALLOWED                               | only channels can be scraped            |
| NO_POST_FOUND                                       | channels With Empty Post                |
| NO_VALID_ID_FOUND                                   | post Id is not Valid                    |
| EXPECT_VALID_CHANNEL_USER_NAMES, AS Query PARAMETER | expect valid multiple channel usernames |
| MULTIPLE_CHANNEL_USER_NAME_EXPECTED                 | channel usernames have to more than 1   |

<br>

## get_info:

<br>

### Path Parameter

| @channel_username |
| ----------------- |

<br>

### Example:

**[Get]** ⚡️ https://fanatgchannelscraper.herokuapp.com/api/get_info/ethio_market_place

<br>

### Response Body:

```js
{
"profile": "https://cdn4.telegram-cdn.org/file/N1p-v7RFqSGbVsBAYKBOkLQ2i8tWmHghTu0gmqGRFLj1FXKcj2Ve0_OO8je_IGWFSDE7qZiRwFubJ8fZbOrOJngvr_Mms6ZGBo-MFXHh7Iivs8MzVB-RPUM64mdvlm4TYGM5FqitDGdkriZKEpv_mf8jU2kOe_IVf5KjHLY7YVayiZ5z8aHCnEFOZnhJkqZOm0woF4bFbXMMSxBLDMJOtHtJ1VvhfYOxkF_cpbhq0Q44c0zndnfRq9x04zdC5DXcbSOtqjzCzsJI6KSKSkAPL3qqJusWb4mQrOSmr6AoMeGqvz8bIcRidtoapkVWYWE5qRTfIDAKtzE2-y0eoNXdXQ.jpg",
"title": "Ethio Market Place",
"username": "@ethio_market_place",
"subscribers": "87",
"photos": "1.94K",
"links": "48"
}

```

<br>

## get_post:

<br>

### Path Parameter

| @channel_username |
| ----------------- |

<br>

### Query Parameter

| offset=[after or before] | post id=[number] |
| ------------------------ | ---------------- |

<br>

### Example:

- **[Get]** ⚡️ https://fanatgchannelscraper.herokuapp.com/api/get_post/ethio_market_place
- **[Get]** ⚡️ https://fanatgchannelscraper.herokuapp.com/api/get_post/ethio_market_place?after=1930
- **[Get]** ⚡️ https://fanatgchannelscraper.herokuapp.com/api/get_post/ethio_market_place?before=1930

<br>

### Response Body Example:

```js
;[
  {
    id: 1937,
    text: '✅ New\n\nCANON ZEBRA ZOOM 100-400MM LENS\n\nCanon zebra zoom 100-400mm lens\nF/4.5-5.6\nAlmost new \n \n ይደውሉልን 0911156257\nካሜራ እና የካሜራ እቃዎችን እንገዛለን እንሸጣለን\n#camera \nከታች ባለው ቴሌግራም ሊንክ ያገኙ https://t.me/joinchat/AAAAAEUTeB3LSYVFukiuQw\n\nአድራሻ= ቦሌ ወሎ ሰፈር HMM ህንፃ 2ኛ ፍቅ 205\n@minilke\n\n💵  BIRR\n\n📱 0911156257 |\n\nFrom: @ethio_market_place_bot',
    img: 'https://cdn4.telegram-cdn.org/file/p4rxUpLuhun-1Ebx_RlDXhe8whUcXuTidRplhQf0NIZUzHb-5LwQv0hC7UzjZqv7PoDDo8x5vs5faKTgko0DPXvqdCE4F089ep8F76fFBRQh1sInwES7J0yVlwrsQeuU0ybFIK_gFMpVlkRFSamMZorN0XVCAaFe_QF-4cMXMv-4jMl7-l6M-ZgzqhzxHD1p5t2xNYHKnLQV3KUilxRnvryiRDnHhrpC4w8ZPHK3i_pK-EFzKPzgMJDzQBdnFZAtx8RYLPD5IawIWvlJQzjEQSQnwHPNhlOEuTyfdlq2NkR3GX-HdButusm8wk4jkNDL1QUisUf1Ju4e-7wyPqDPiA.jpg',
  },
]
```

<br>

## channel_value:

<br>

### Path Parameter

| @channel_username |
| ----------------- |

<br>

### Query Parameter

| offset=[after or before] | post id=[number] |
| ------------------------ | ---------------- |

<br>

### Example:

- **[Get]** ⚡️ https://fanatgchannelscraper.herokuapp.com/api/channel_value/ethio_market_place
- **[Get]** ⚡️ https://fanatgchannelscraper.herokuapp.com/api/channel_value/ethio_market_place?after=1930
- **[Get]** ⚡️ https://fanatgchannelscraper.herokuapp.com/api/channel_value/ethio_market_place?before=1930

<br>

### Response Body Example:

```js
;[
  {
    img: 'https://cdn4.telegram-cdn.org/file/MEUpI2TCs_TqQHHFLyDqBh9Ng1bg9bjmFyPP7ApjuIMyHvoeKXTgQbxeJG1shl2wAswuNc_DVqH3_Yyk0Uh8shu2OzAoYhI677j7FZ6F8Xt4ikWjY7lD6XeW7oB_4dDehahVm7_jplHSst4HkBtDZSkyTQjZykhxZ0IBWWnVt_5Cw4kQJECXqFmpoI9AVddFe83vi_90ZrQse4UbMeqki0ViM-P1L2v7LxCcfHjRGMFLTYY8wXdI0XMTPjXAt5v_jsoeSHKfP3bHsWN_zkTGQLatuuQAp6zt6Y2wqKZvvrWfNYtPaIoSXa6zvgOmRfC9gU1Zks5ztiK1UeoP94idSg.jpg',
    scriped_id: 1930,
    description: 'Available on hand \n  👉@bintejemal\n  👉Price = 700',
    title: 'Available on hand ',
    price: ['700'],
  },
]
```

<br>

## getlastpost_id:

<br>

### Path Parameter

| @channel_username |
| ----------------- |

<br>

### Query Parameter

| offset=[after or before] | post id=[number] |
| ------------------------ | ---------------- |

<br>

### Example:

- **[Get]** ⚡️ https://fanatgchannelscraper.herokuapp.com/api/getlastpost_id/ethio_market_place
- **[Get]** ⚡️ https://fanatgchannelscraper.herokuapp.com/api/getlastpost_id/ethio_market_place?after=1930
- **[Get]** ⚡️ https://fanatgchannelscraper.herokuapp.com/api/getlastpost_id/ethio_market_place?before=1930

<br>

### Response Body Example:

```js
{
 "last_post_id": 1956;
}
```

<br>

## getpostby_id:

<br>

### Path Parameter

| @channel_username | post id |
| ----------------- | ------- |

<br>

### Example:

- **[Get]** ⚡️ https://fanatgchannelscraper.herokuapp.com/api/getpostby_id/ethio_market_place/1954

<br>

### Response Body Example:

```js
{
"photo": "https://cdn4.telegram-cdn.org/file/MXBpS8E3YNH-0NYhFk8M76KUjiT-CnsLkJFDfBLfS-4j-3rI3nEvml2CR3Gvu0m1McG6DjApCp3d8W2sHzIVK_51VI58YseWB3_FWjObH0dd21_aDuMOgdOI0m42pAtqf_NZI70pr6X-ctSOMBQhwwstBnHFgkhsUI5mVnaOkMXaJ2b3bDvqGLORBXAVTpsf-ulfSgDV_SlUnz8mwsO20K6PdBjVxVtSxSQjpCdWCALM_cZLpStX4mTOHJK3jW8BS2cxjl_elN_KRo-bRSGUQYBAEszCIX4_2xzhjEbtvGbN9DjMXl_6u0m-8IS4DALbLLWs8luO5IIHWZI6ia_aqQ.jpg",
"text": "✅ New\n\nCANON 5D MARK  IV \n\nCanon 5D mark  IV \nOnly body \n \n ይደውሉልን 0911156257\nካሜራ እና የካሜራ እቃዎችን እንገዛለን እንሸጣለን\n#camera \nከታች ባለው ቴሌግራም ሊንክ ያገኙ https://t.me/joinchat/AAAAAEUTeB3LSYVFukiuQw\n\nአድራሻ= ቦሌ ወሎ ሰፈር HMM ህንፃ 2ኛ ፍቅ 205\n@minilke\n\n💵  BIRR\n\n📱 0911156257 |\n@\n\n#NEW\n\nFrom: @ethio_market_place_bot"
}
```

<br>

## getmultiplechannels_post:

<br>

### Query Parameter

| @channel username 1 | @channel username 2 | .... |
| ------------------- | ------------------- | ---- |

<br>

### Example:

- **[Get]** ⚡️ https://fanatgchannelscraper.herokuapp.com/api/getmultiplechannels_post?channels=ethio_market_place&channels=ethio_market_place

<br>

```js
;[
  [
    {
      id: 1939,
      text: '✅ New\n\nBRAND NEW GODOX \n\nBRAND NEW GODOX \nAD600BM\noutdoor spot\n \n ይደውሉልን 0911156257\nካሜራ እና የካሜራ እቃዎችን እንገዛለን እንሸጣለን\n#camera \nከታች ባለው ቴሌግራም ሊንክ ያገኙ https://t.me/joinchat/AAAAAEUTeB3LSYVFukiuQw\n\nአድራሻ= ቦሌ ወሎ ሰፈር HMM ህንፃ 2ኛ ፍቅ 205\n@minilke\n\n💵  BIRR\n\n📱 0911156257 |\n@undefined\n\n#undefined\n\nFrom: @ethio_market_place_bot',
      img: 'https://cdn4.telegram-cdn.org/file/aysdQGzUgH5w0ZR40u90QN1QfOkWU1wlAqwrzrIkRdJJwEF1jU16k50hJY-8anmwK6If0F7CngLUVoczllBIsLQjXopYMYSMtNwu1SBcO7mhcpgvyIXBzuFN2Fr9-SX8oMr4TDNQVp6dpAaEcdAw_9O0z3Muj8TT1QcdZLNFw-PXv29sBIKkAMc9Xb7GfnOKHk_d-dbbC-pGCg32ORAL3cXuSKAH3xZu1dGtc6820GnOWBE7VrWoHdmJ4UYW0xhnUZD_8FX-RWacrTuk_Oha-l-yA73X23kPtiP44F58dLIyKiwnOr0skTNwKQnmJ_AbozISmen27M0yR2OFegyZJQ.jpg',
    },{....}
  ],
  [
    {
      id: 1937,
      text: '✅ New\n\nCANON ZEBRA ZOOM 100-400MM LENS\n\nCanon zebra zoom 100-400mm lens\nF/4.5-5.6\nAlmost new \n \n ይደውሉልን 0911156257\nካሜራ እና የካሜራ እቃዎችን እንገዛለን እንሸጣለን\n#camera \nከታች ባለው ቴሌግራም ሊንክ ያገኙ https://t.me/joinchat/AAAAAEUTeB3LSYVFukiuQw\n\nአድራሻ= ቦሌ ወሎ ሰፈር HMM ህንፃ 2ኛ ፍቅ 205\n@minilke\n\n💵  BIRR\n\n📱 0911156257 |\n\nFrom: @ethio_market_place_bot',
      img: 'https://cdn4.telegram-cdn.org/file/p4rxUpLuhun-1Ebx_RlDXhe8whUcXuTidRplhQf0NIZUzHb-5LwQv0hC7UzjZqv7PoDDo8x5vs5faKTgko0DPXvqdCE4F089ep8F76fFBRQh1sInwES7J0yVlwrsQeuU0ybFIK_gFMpVlkRFSamMZorN0XVCAaFe_QF-4cMXMv-4jMl7-l6M-ZgzqhzxHD1p5t2xNYHKnLQV3KUilxRnvryiRDnHhrpC4w8ZPHK3i_pK-EFzKPzgMJDzQBdnFZAtx8RYLPD5IawIWvlJQzjEQSQnwHPNhlOEuTyfdlq2NkR3GX-HdButusm8wk4jkNDL1QUisUf1Ju4e-7wyPqDPiA.jpg',
    },{....}
  ],
]
```

<br>

**Contact :**
⚡️ [Abdi Urgessa](https://t.me/Me_abd)
