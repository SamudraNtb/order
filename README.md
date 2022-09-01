# orderelif cmd == "order" or text.lower() == 'promo':                            	
                                contact = cl.getProfile()
                                mids = [contact.mid]
                                tz = pytz.timezone("Asia/Jakarta")
                                timeNow = datetime.now(tz=tz)
                                status = cl.getContact(sender)                   
                                cover = cl.getProfileCoverURL(sender)
                                data = {
  "type": "carousel",
  "contents": [
    {
      "type": "bubble",
      "size": "kilo",
      "body": {
        "type": "box",
        "layout": "vertical",
        "contents": [
          {
            "type": "image",
            "size": "full",
            "aspectMode": "cover",
            "aspectRatio": "6:12",
            "gravity": "top",
            "url": "https://a.top4top.io/p_2210wfvfk0.gif"
          },
          {
            "type": "box",
            "layout": "vertical",
            "contents": [
              {
                "type": "text",
                "text": ","
              },
              {
                "type": "image",
                "url": "https://obs.line-scdn.net/{}".format(cl.getContact(mid).pictureStatus),
                "size": "full",
                "aspectMode": "cover",
                "offsetBottom": "22px"
              }
            ],
            "position": "absolute",
            "width": "69px",
            "height": "69px",
            "borderWidth": "1px",
            "borderColor": "#000000",
            "cornerRadius": "100px",
            "offsetTop": "442px",
            "offsetStart": "183px"
          },
          {
            "type": "box",
            "layout": "vertical",
            "contents": [
              {
                "type": "text",
                "text": "  Promo  ",
                "size": "xxs",
                "color": "#ffffff",
                "weight": "bold"
              }
            ],
            "position": "absolute",
            "offsetTop": "6px",
            "offsetStart": "184px",
            "borderWidth": "1px",
            "borderColor": "#ffffff",
            "cornerRadius": "5px",
            "backgroundColor": "#000000"
          },
          {
            "type": "box",
            "layout": "vertical",
            "contents": [
              {
                "type": "text",
                "text": "╭───────────────\n│╭──────────────\n│├• ᴛᴇʀɪᴍᴀᴋᴀsɪʜ\n│├• sᴀмuᴅʀᴀ\n│╰──────────────\n├──•〔 ᴏ ᴘ ᴇ ɴ ʀ ᴇ ɴ ᴛ ᴀ ʟ 〕\n│╭──────────────\n│├─•  sᴇʟғʙᴏᴛ :\n││( 𝟏 )• ғᴜʟʟ ᴛᴇᴍᴘʟᴀᴛᴇ\n││( 𝟐 )• ɴᴏ ᴛᴇᴍᴘʟᴀᴛᴇ\n│├─•  ᴘʀᴏᴛᴇᴄᴛ / ᴡᴀʀ :\n││( 𝟏 )• 𝟑 ᴀssɪsᴛ\n││( 𝟐 )• 𝟓 ᴀssɪsᴛ\n││( 𝟑 )• 𝟕 ᴀssɪsᴛ\n││( 𝟒 )• ᴄʟɪᴇɴᴛ ᴘʀᴏᴛᴇᴄᴛ\n│╰──────────────\n├──•〔 sᴇʟʟ   ᴛʜᴇ   sᴄʀɪᴘᴛ 〕\n│╭──────────────\n││( 𝟏 )• ʜᴇʟᴘᴇʀs\n││( 𝟐 )• sʙ ᴡᴀʀ\n││( 𝟑 )• sʙ ᴘʀᴏᴛᴇᴄᴛ\n││( 𝟒 )• ᴄʟ/ᴄʟɪᴇɴᴛ\n││( 𝟓 )• sʙ ғᴜʟʟ ᴛᴇᴍᴘʟᴀᴛᴇ\n│╰──────────────\n│ ན ᴄʀ : line://ti/p/~zeuszx.py\n╰───────────────",
                "size": "xxs",
                "color": "#ffffff",
                "weight": "bold",
                "decoration": "underline",
                "align": "center",
                "wrap": True,
              }
            ],
            "position": "absolute",
            "offsetTop": "60px",
            "offsetStart": "5px"
          },
          {
            "type": "box",
            "layout": "vertical",
            "contents": [
              {
                "type": "text",
                "text": ""+ datetime.strftime(timeNow,'%Y-%m-%d'),
                "size": "xxs",
                "color": "#ffffff",
                "weight": "bold"
              },
              {
                "type": "text",
                "text": ""+ datetime.strftime(timeNow,'%H:%M:%S'),
                "size": "xxs",
                "color": "#ffffff",
                "weight": "bold"
              }
            ],
            "position": "absolute",
            "offsetTop": "2px",
            "offsetStart": "5px"
          },
          {
            "type": "box",
            "layout": "vertical",
            "contents": [
              {
                "type": "text",
                "text": "{}".format(cl.getContact(mid).displayName),
                "size": "xxs",
                "color": "#ffffff",
                "weight": "bold",
                "offsetStart": "75px",
                "offsetTop": "1px"
              }
            ],
            "backgroundColor": "#000000"
          }
        ],
        "paddingAll": "0px",
        "borderWidth": "1px",
        "borderColor": "#C0C0C0",
        "cornerRadius": "10px",
        "action": {
          "type": "uri",
          "label": "action",
          "uri": "http://line.me/ti/p/~zeuszx.py"
        }
      }
    }
  ]
}
                                cl.postFlex(to, data)
