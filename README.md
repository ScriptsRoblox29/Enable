local StarterGui = game:GetService("StarterGui")

local guiList = {
    Enum.CoreGuiType.Backpack,
    Enum.CoreGuiType.Chat,
    Enum.CoreGuiType.Health,
    Enum.CoreGuiType.PlayerList,
    Enum.CoreGuiType.EmotesMenu,
    Enum.CoreGuiType.Backpack,
}

for _, gui in ipairs(guiList) do
    StarterGui:SetCoreGuiEnabled(gui, true)

    StarterGui:SetCore("SendNotification", {
        Title = "Enabled " .. gui.Name,
        Text = "Activated successfully",
        Duration = 3
    })

    task.wait(0.1)
end

StarterGui:SetCore("SendNotification", {
    Title = "Completed!",
    Text = "All options have been activated.",
    Duration = 7.5
})

StarterGui:SetCoreGuiEnabled(Enum.CoreGuiType.All, true)
