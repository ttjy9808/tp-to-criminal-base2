localplayer = game.Players.LocalPlayer
 Char = localplayer.Character or workspace:FindFirstChild(localplayer.Name)
         HRP = Char and Char:FindFirstChild("HumanoidRootPart")
        if not Char or not HRP then
           
        end
         p = HRP.Position
         hrd = game.Players.LocalPlayer.Character.HumanoidRootPart
         x = 40.25
         y = 25.24
       	 z = -146.05
        hrd.CFrame = CFrame.new(p.x, 1000, p.z)
         currentPos = Vector3.new(p.x, 1000, p.z)
         targetPos = Vector3.new(x, 1000, z)

         direction = (targetPos - currentPos).Unit
         distance = (targetPos - currentPos).Magnitude
         steps = math.floor(distance / 10) 
        for j = 1, steps do
            currentPos = currentPos + direction * 10
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(currentPos)
            task.wait()
        end

        
        currentPos = targetPos
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(currentPos)
         p = hrd.Position
        
         currentPos = Vector3.new(x, 1000, z)
         targetPos = Vector3.new(x, y, z)

         direction = (targetPos - currentPos).Unit
         distance = (targetPos - currentPos).Magnitude
         steps = math.floor(distance / 10) 
        for i = 1, steps do
            currentPos = currentPos + direction * 10 
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(currentPos)
            task.wait()
        end
