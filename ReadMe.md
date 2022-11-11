# ⚡️ TELEGRAM CHANNEL SCRAPER ⚡️

> [Updated Version Of Fana Protocol](https://github.com/baydisng13/fana-doc/blob/main/README.md)

> Base Url : https://fanatgchannelscraper.herokuapp.com/api/v2

<br>

## End-Points:

- ⚡️`get_info/{channel_username}`
- ⚡️`get_post/{channel_username}`
- ⚡️`get_posts/{channel_username}`
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
| CONNECTION_ERROR_FOUND                              | connection problem occured              |

<br>

## get_info:

<br>

### Path Parameter

| @channel_username |
| ----------------- |

<br>

### Example:

**[Get]** ⚡️ https://fanatgchannelscraper.herokuapp.com/api/v2/get_info/ethio_market_place

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

## get_post && get_posts:

<br>

### Path Parameter

| @channel_username |
| ----------------- |

<br>

### Query Parameter

| offset=[after or before] | post id=[number] |
| ------------------------ | ---------------- |

<br>

### Example get_post:

- **[Get]** ⚡️ https://fanatgchannelscraper.herokuapp.com/api/v2/get_post/ethio_market_place
- **[Get]** ⚡️ https://fanatgchannelscraper.herokuapp.com/api/v2/get_post/ethio_market_place?after=1930
- **[Get]** ⚡️ https://fanatgchannelscraper.herokuapp.com/api/v2/get_post/ethio_market_place?before=1930

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

### Example get_posts:

- **[Get]** ⚡️ https://fanatgchannelscraper.herokuapp.com/api/v2/get_posts/behagerlij
- **[Get]** ⚡️ https://fanatgchannelscraper.herokuapp.com/api/v2/get_posts/behagerlij?after=500
- **[Get]** ⚡️ https://fanatgchannelscraper.herokuapp.com/api/v2/get_posts/behagerlij?before=500

<br>

### Response Body Example:

```js
;[
  {
    id: 524,
    text: 'The small things add up to make big differences. \nIt’s all about the little things.\n.\n.\n.\n#behagerlij #awaqi #illustration #Ethiopia',
    img: [
      'https://cdn4.telegram-cdn.org/file/SlX7hTBMwd_wcogFUhmwou7EZrbexrdc7LTOhoNATO8J6L8lsp_HUAU_3GOqXvLg1MWbPyzwacx9E2LJoRdDmdwe94sp8IRSqQiVcyLNCd9gXtla0ClEulLbT14eFyAZ6s2LxjtpaT3UNRlbOKZS90_eHcUzWp2_DZXTTjRkcq1lzPGKk-URarEYKvVflGI5S0ejxZWrpdRXI06EvTYkgha-fA1uNF6Epm2VuuRLx1-xCkLSb-H_nPqxnkJafKnizULGfzIKi_wy-Ly51uv189ilHkbYNxBhbGS9uNIE16rA3oyF_wl8tczUQzi7xxytKN-rVqysWlBSblwAC507dg.jpg',
      'https://cdn4.telegram-cdn.org/file/mbmniacrOq_68OXDI85Do1nkv10fZxS0bFf4fKbfsDpO8ZNCxptXVR_hqg4Dz65DGixZikmqWBRz8I5U8mKmDBAvU2g3NXl1iPHj3cP878rl04-hDGpLCnF8pCAQ__96S_dfiHquFeQOrSyMQ2ZkJyO41NEQDOk_wSZaEMvSon_I8JPwJlP21JQgdhey-KWOXkTKFZCp8kM8xbRt1J4wKthlAxeU3feRbnSqp_XvlcfigXO3RYE5ZrWvp9BqXAUDWQxqPqd9j6_ciosrUvMTRPXreBLvePkh19sKyqc3QFcfJMKSi64ZVJaCdstN_-yeNMRzPKZhfiylV6RvkPgKRA.jpg',
      'https://cdn4.telegram-cdn.org/file/MoQILD8OfJV_JmQEP2qDYHRvT3KB-XNmzIkp103ZiClcG4Ac1nA10jMhvmBU1jiAryYqyGVgjhSZXKd7ax4isBGb5ezhNYk-FeRnRUDdkmzn_3aweFlrC_v9HyJK8asRDIWpc6e2QWEpiYHYWjCIq7N6GeJCrhZsCiHGqGkbFfxp5YIJJn3M8dWCIplWqbtn6zXgXyR7VEhDedfEVVjpBFzEMDAlv26SVeLk-yhIUu-2F2soYhmfWmXSvGG6xNYIZylCprLEPfbRbt88B76P893CCNJ0f8KlTkb3UsVvfsn7B55COpm_cgDX2go2SZm2Sxf4f_d3m5M6H4dS9t5vdw.jpg',
      'https://cdn4.telegram-cdn.org/file/iQ7MFLjLoDdYasd4peL_xVL8_41Ypc5hOnw_gfzUasKLY3JukrZYGH6c_bnwF4FDNwVuOZVOpHHi3HbwXLqbpyH2YzHnWxK509EHkiI-54BljQzXdCrCHfMUzZe9k3VWCD0WxhFKdSqmx2XZLrvnf60A7qpctFk5p9b1Wz2MU_gI93gCnLCXqAVosJRWrVINzfqHZNBgtrl92JRxgbLGqYRBjrDDcGx-G26UYWakGEVuEQpGd-PJYDIKSmN3VTClvy9_vRoaDkwYhvAEMV21XUOB1D9yjZjSdslM-Ta4KN2Jq_75MhWwrr4JZYm2JehKzH0yq12v_XhRLgp1v7k99A.jpg',
      'https://cdn4.telegram-cdn.org/file/quxagxgTkG9qAvgWFGS4CMqVH4Xv91WIqxYmmcYoGSQV5BK8iABtiOL5QsCdJfw71P2mP5xqzzNl0m2S9VL-CejEgMvjfKwygv47j1eZ46DsveI3o51u-va0mzi0JROe6lzBVXGYueCqPc0te177UJh4dXoxF_OOMT_DhenX-I9ENMlA20mQ842uKGETnbR2OJLxr2dpFBYV8g34EcCi-EpzfE1hHPSIGB9XZPgY1TQW_WoshQEHdq0iKUjU_Io0NXoOhvOhWCVI5uIxwwWx3ATO1U4PaOeX4_R-5a_jZkoGN5lW-Pz1GwDbbuUkgWUbLIOgKK29_wC3U6syNOuqyQ.jpg',
    ],
    vid: [],
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

- **[Get]** ⚡️ https://fanatgchannelscraper.herokuapp.com/api/v2/channel_value/ethio_market_place
- **[Get]** ⚡️ https://fanatgchannelscraper.herokuapp.com/api/v2/channel_value/ethio_market_place?after=1930
- **[Get]** ⚡️ https://fanatgchannelscraper.herokuapp.com/api/v2/channel_value/ethio_market_place?before=1930

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

- **[Get]** ⚡️ https://fanatgchannelscraper.herokuapp.com/api/v2/getlastpost_id/ethio_market_place
- **[Get]** ⚡️ https://fanatgchannelscraper.herokuapp.com/api/v2/getlastpost_id/ethio_market_place?after=1930
- **[Get]** ⚡️ https://fanatgchannelscraper.herokuapp.com/api/v2/getlastpost_id/ethio_market_place?before=1930

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

- **[Get]** ⚡️ https://fanatgchannelscraper.herokuapp.com/api/v2/getpostby_id/ethio_market_place/1954

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

- **[Get]** ⚡️ https://fanatgchannelscraper.herokuapp.com/api/v2/getmultiplechannels_post?channels=ethio_market_place&channels=ethio_market_place

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
