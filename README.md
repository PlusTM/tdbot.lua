# tdbot.lua
A simple Lua library for the [`telegram-bot`](https://valtman.name/telegram-bot).
just an update based on [`telegram-cli library`](https://github.com/rizaumami/tdcli.lua) for new TG.

documentation >> [soon...](https://github.com/i-naji/tdbot.lua/wiki) 

## How to Use

See example script below.

- Place this `tdbot.lua` file inside the same folder as your bot, or anywhere else as long as you import it properly.
- Import it into your bot.
- Call the functions.

See example script below.

```lua
-- Load tdbot library.
tdbot = dofile('tdbot.lua')


function tdbot_update_callback (data)
  if (data._ == "updateNewMessage") then
    local msg = data.message
    if msg.content._ == "messageText" then
      if msg.content.text == "ping" then
	tdbot.sendText(msg.chat_id, 0, true, true, nil, "PONG")
      end
    end
  end
end

```

## The Functions

`tdbot.lua` is a Work In Progress. This commit is based on [telegram-bot-170901.tl](https://valtman.name/files/telegram-bot-170901-nightly.tl) scheme.
Here is a list of functions that's should works.

- [x] getAuthState
- [x] setAuthPhoneNumber
- [x] resendAuthCode
- [x] checkAuthCode
- [x] checkAuthPassword
- [x] requestAuthPasswordRecovery
- [x] recoverAuthPassword
- [x] resetAuth
- [x] checkAuthBotToken
- [x] getPasswordState
- [x] setPassword
- [x] getRecoveryEmail
- [x] setRecoveryEmail
- [x] requestPasswordRecovery
- [x] recoverPassword
- [x] createTemporaryPassword
- [x] getMe
- [x] getUser
- [x] getUserFull
- [x] getGroup
- [x] getGroupFull
- [x] getChannel
- [x] getChannelFull
- [x] getSecretChat
- [x] getChat
- [x] getMessage
- [x] getMessages
- [x] getFile
- [x] getFilePersistent
- [x] getChats
- [x] searchPublicChat
- [x] searchPublicChats
- [x] searchChats
- [x] getTopChats
- [x] deleteTopChat
- [x] addRecentlyFoundChat
- [x] deleteRecentlyFoundChat
- [x] deleteRecentlyFoundChats
- [x] getCommonChats
- [x] getCreatedPublicChats
- [x] getChatHistory
- [x] deleteChatHistory
- [x] searchChatMessages
- [x] searchMessages
- [x] searchSecretMessages
- [x] searchCallMessages
- [x] getPublicMessageLink
- [x] sendBotStartMessage
- [x] sendInlineQueryResultMessage
- [x] forwardMessages
- [x] sendChatScreenshotTakenNotification
- [x] sendChatSetTtlMessage
- [x] deleteMessages
- [x] deleteMessagesFromUser
- [x] editMessageText
- [x] editMessageCaption
- [x] editMessageReplyMarkup
- [x] editInlineMessageText
- [x] editInlineMessageCaption
- [x] editInlineMessageReplyMarkup
- [x] getTextEntities
- [x] getFileMimeType
- [x] getInlineQueryResults
- [x] answerInlineQuery
- [x] getCallbackQueryAnswer
- [x] answerCallbackQuery
- [x] answerShippingQuery
- [x] answerPreCheckoutQuery
- [x] setGameScore
- [x] setInlineGameScore
- [x] getGameHighScores
- [x] getInlineGameHighScores
- [x] deleteChatReplyMarkup
- [x] sendChatAction
- [x] openChat
- [x] closeChat
- [x] viewMessages
- [x] openMessageContent
- [x] createPrivateChat
- [x] createGroupChat
- [x] createChannelChat
- [x] createSecretChat
- [x] createNewGroupChat
- [x] createNewChannelChat
- [x] createNewSecretChat
- [x] migrateGroupChatToChannelChat
- [x] changeChatTitle
- [x] changeChatPhoto
- [x] changeChatDraftMessage
- [x] toggleChatIsPinned
- [x] setChatClientData
- [x] addChatMember
- [x] addChatMembers
- [x] changeChatMemberStatus
- [x] getChatMember
- [x] searchChatMembers
- [x] setPinnedChats
- [x] downloadFile
- [x] cancelDownloadFile
- [x] uploadFile
- [x] cancelUploadFile
- [x] setFileGenerationProgress
- [x] finishFileGeneration
- [x] exportChatInviteLink
- [x] checkChatInviteLink
- [x] importChatInviteLink
- [x] createCall
- [x] acceptCall
- [x] rateCall
- [x] blockUser
- [x] unblockUser
- [x] getBlockedUsers
- [x] importContacts
- [x] searchContacts
- [x] deleteContacts
- [x] getUserProfilePhotos
- [x] getStickers
- [x] getInstalledStickerSets
- [x] getArchivedStickerSets
- [x] getTrendingStickerSets
- [x] getAttachedStickerSets
- [x] getStickerSet
- [x] searchStickerSet
- [x] changeStickerSet 
- [x] viewTrendingStickerSets
- [x] reorderInstalledStickerSets
- [x] getRecentStickers
- [x] addRecentSticker
- [x] deleteRecentSticker
- [x] clearRecentStickers
- [x] getStickerEmojis
- [x] getSavedAnimations
- [x] addSavedAnimation
- [x] deleteSavedAnimation
- [x] getRecentInlineBots
- [x] searchHashtags
- [x] deleteRecentHashtag
- [x] getWebPagePreview
- [x] getWebPageInstantView
- [x] getNotificationSettings
- [x] setNotificationSettings
- [x] resetAllNotificationSettings
- [x] setProfilePhoto
- [x] deleteProfilePhoto
- [x] changeName
- [x] changeAbout
- [x] changeUsername
- [x] changePhoneNumber
- [x] resendChangePhoneNumberCode
- [x] checkChangePhoneNumberCode
- [x] getActiveSessions
- [x] terminateSession
- [x] terminateAllOtherSessions
- [x] toggleGroupEditors
- [x] changeChannelUsername
- [x] toggleChannelInvites
- [x] toggleChannelSignMessages
- [x] changeChannelAbout
- [x] pinChannelMessage
- [x] unpinChannelMessage
- [x] reportChannelSpam
- [x] getChannelMembers
- [x] deleteChannel
- [x] closeSecretChat
- [x] getChatEventLog
- [x] getPaymentForm
- [x] validateOrderInfo
- [x] sendPaymentForm
- [x] getPaymentReceipt
- [x] getSavedOrderInfo
- [x] deleteSavedOrderInfo
- [x] deleteSavedCredentials
- [x] getSupportUser
- [x] getWallpapers
- [x] registerDevice
- [x] setPrivacy
- [x] getPrivacy
- [x] getOption
- [x] setOption
- [x] changeAccountTtl
- [x] getAccountTtl
- [x] deleteAccount
- [x] getChatReportSpamState
- [x] changeChatReportSpamState
- [x] reportChat
- [x] getStorageStatistics
- [x] getStorageStatisticsFast
- [x] optimizeStorage
- [x] setNetworkType
- [x] getNetworkStatistics
- [x] addNetworkStatistics
- [x] resetNetworkStatistics
- [x] setBotUpdatesStatus
- [x] uploadStickerFile
- [x] createNewStickerSet
- [x] addStickerToSet
- [x] setStickerPositionInSet
- [x] deleteStickerFromSet
- [x] sendCustomRequest
- [x] answerCustomQuery
- [x] sendCustomRequest
- [x] setAlarm
- [x] getInviteText
- [x] getTermsOfService
- [x] setProxy
- [x] getProxy
- [x] sendText
- [x] sendAnimation
- [x] sendAudio
- [x] sendDocument
- [x] sendPhoto
- [x] sendSticker
- [x] sendVideo
- [x] sendVideoNote
- [x] sendVoice
- [x] sendLocation
- [x] sendVenue
- [x] sendContact
- [x] sendGame
- [x] sendInvoice
- [x] sendForwarded
