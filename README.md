# HomeAssistant_NodeRed
Home Assistant Node Red flows

## Garden Irrigation

Flow to trigger the garden water system automatically twice a day. Will eventually add humidity + temperature sensor information in order to adjust watering minutes for every time. Also includes notification for manual watering of plants with no automatic irrigation system (plants inside the house). Will also eventually add humidity + temperature data to notify only when needed. Added notifications in case watering fails to trigger or fails to stop. Sensor to use: Xiaomi Mi Flora (bluetooth) [MiFlora component for Home Assistant](https://www.home-assistant.io/components/miflora)

[Irrigation Flow](https://github.com/julietsvq/HomeAssistant_NodeRed/blob/master/garden%20irrigation%20flow.json)
![Irrigation Flow image](https://github.com/julietsvq/HomeAssistant_NodeRed/blob/master/images/garden_irrigation.png)

## Notifications

This flow sends notifications via IFTTT webhooks when certain events happen (when away garaje door left open or lights left on). Initially I was using notifications via Telegram insead, but IFTTT app push notifications are better for this purpose.

[Notifications Flow](https://github.com/julietsvq/HomeAssistant_NodeRed/blob/master/notifications%20flow.json)
![Notifications Flow image](https://github.com/julietsvq/HomeAssistant_NodeRed/blob/master/images/notifications.png)

## Dash Button

As Amazon discontinued physical Dash Buttons, created a flow to make use of it as a wifi button. In this case, to open / close the shades as I have no physical switch to do so. Requires the [dasshio component for Home Assistant](https://github.com/danimtb/dasshio). You can change it to apply to another entity by changing the configuration of the dasshio component. As I have no isclosed in the shades entity's state, I created and input boolean as an indicator to know which action the button should perform (set to toggle). The boolean will change value if shades are opened or closed using other devices (voice assistant for example) as well.

[Dash Button Flow](https://github.com/julietsvq/HomeAssistant_NodeRed/blob/master/dash%20button%20flow.json)
![Dash Button Flow image](https://github.com/julietsvq/HomeAssistant_NodeRed/blob/master/images/dash_button.png)


## Cat Litter Reminder

To make sure everyone at home takes turns at cleaning the cat litter box, this flow sends a notification via IFTTT mobile push notification every morning at 9.15, and repeats it 6 hours later or until that person is back home if it still hasn't been cleaned. If it is cleaned at any other point all timers are cancelled until next day.

[Cat Litter Flow](https://github.com/julietsvq/HomeAssistant_NodeRed/blob/master/cat%20litter%20flow.json)
![Cat Litter Flow image](https://github.com/julietsvq/HomeAssistant_NodeRed/blob/master/images/cat_litter.png)

## Air

Will automatically turn off the air conditioning after 00.00 if left on.

[Air Flow](https://github.com/julietsvq/HomeAssistant_NodeRed/blob/master/office%20air%20flow.json)
![Air Flow image](https://github.com/julietsvq/HomeAssistant_NodeRed/blob/master/images/air.png)

## Daily Backup

Automatically take Home Assistant backup every day and save to DropBox.

[Daily Backup Flow](https://github.com/julietsvq/HomeAssistant_NodeRed)
![Daily Backup Flow image](https://github.com/julietsvq/HomeAssistant_NodeRed/blob/master/images/nightly_backups.png)
