# Quantum
Atomically oriented 4D Engine. Relies on a simple rule-set that pushes state-modification work onto the GPU using pure functions.

Made with 🔥 by kasai

## Example kasai script:
```kasai
import quantum where informal

assume quantum is tested
assume quantum.version > 0.0.5

Quantum Item Demo:
  Centered Label greeting: "Hello World"
  Planet world: Burning

  when this is visible:
    show: greeting
  
  when greeting.age > 20s:
      greeting.fade_out()
      
      show: world
      world.vibrate:
        displacement: world.radius / 2
      
      greeting: "Raze the World"
      greeting.fade_in()
    
  when world.age = 0.5m:
    world.collapse(Direction.inwards)
    
    world.fade_out(3s)
    
    
Add: Demo(position:location.origin)
```

# Example informal kasai script:
```kasai
import quantum

assume quantum is tested
assume quantum.version > 0.0.2


def Burning Planet:
  when this is Visible:
    when age is between(30s, 1m):
      position is Vibrating by (radius / 2)
    
    when age > 1m:
      this is Collapsing Inwards
      
      this is Fading Out

Burning Planet earth: 
  Hidden
  position: greeting.bottom

Signpost greeting: "Hello World"
  position: location.origin
  
when greeting.age > 3s:
  earth is Visible
    
```

