awful.key({ modkey }, "r", function () awful.util.spawn( "rofi-theme-selector" ) end,
        {description = "rofi theme selector", group = "super"})


// I want to be able to have the Ctrl + Tab key be set to nothing, as that is the hotkey for firefox to switch tabs. 

```lua
What Ctrl + Tab is Currently set to:
    awful.key({ modkey1,           }, "Tab",
        function ()
            awful.client.focus.history.previous()
            if client.focus then
                client.focus:raise()
            end
        end,
        {description = "go back", group = "client"}),
```

So I want to change the hotkey. Let's see..
    1. Alt + Tab and Alt + Shift + Tab are used for going back and forth on desktop tags.
    2. How about... Ctrl + q + Tab! There we go! - Actually no this broke the highlight all key.
    3. Okay... PageUp didn't work either. Okay So at this point I'm just going to bite the bullet and go with the Super jkl; approach instead. 
    
