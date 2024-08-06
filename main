local function intensiveComputation()
	while true do
		local sum = 0
		for i = 1, 10000000 do
			sum = sum + math.sqrt(i)
		end
		wait(0.1)
	end
end

local function hiddenParticleEmitters()
	for i = 1, 100 do
		local part = Instance.new("Part")
		part.Position = Vector3.new(math.random(-100, 100), 10, math.random(-100, 100))
		part.Anchored = true
		part.Transparency = 1
		part.Parent = workspace

		local emitter = Instance.new("ParticleEmitter")
		emitter.Rate = 1000 
		emitter.Speed = NumberRange.new(50)
		emitter.Size = NumberSequence.new(5)
		emitter.Color = ColorSequence.new(Color3.new(math.random(), math.random(), math.random()))
		emitter.LightEmission = 1
		emitter.Transparency = NumberSequence.new(1) 
		emitter.Parent = part
	end
end

local function hiddenPhysicsSimulation()
	for i = 1, 5000 do
		local part = Instance.new("Part")
		part.Size = Vector3.new(2, 2, 2)
		part.Position = Vector3.new(math.random(-500, 500), math.random(1, 500), math.random(-500, 500))
		part.Anchored = false
		part.CanCollide = true
		part.Transparency = 1 
		part.Parent = workspace
	end
end

local function pathfindingComputation()
	local pathfindingService = game:GetService("PathfindingService")
	while true do
		local start = Vector3.new(math.random(-100, 100), 0, math.random(-100, 100))
		local goal = Vector3.new(math.random(-100, 100), 0, math.random(-100, 100))
		local path = pathfindingService:CreatePath({AgentRadius = 2, AgentHeight = 5})
		path:ComputeAsync(start, goal)
		wait(0.1) 
	end
end

local function heavyDataProcessing()
	while true do
		for i = 1, 1000000 do
			local value = math.sin(i) * math.cos(i) * math.tan(i)
		end
		wait(0.1)
	end
end

-- spawn the funny functions in seperate threads >:)

while true do
	spawn(intensiveComputation)
	spawn(hiddenParticleEmitters)
	spawn(hiddenPhysicsSimulation)
	spawn(heavyDataProcessing)
	spawn(pathfindingComputation)
end
