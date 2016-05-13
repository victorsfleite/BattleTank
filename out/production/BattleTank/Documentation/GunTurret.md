# Class:

```java
public class GunTurret
```

* This class gathers all the features of enemies turrets.

## Methods:

```java
public GunTurret(double x, double y, double z, int angle)
```  

* This is a constructor method, which is responsible for initializing the turret and has as parameters the coordinates and the angle of the turret.

#### Declarations of GunTurret():
```java
start = new vector(x,y,z);
  iDirection = new vector(0.7,0,0);
  jDirection = new vector(0,0.7,0);
  kDirection = new vector(0,0,0.7);
```

* These declaration define the centre point of this model(also the centre point of tank body)


```java
public void makeBody()
```

* This method is responsible for create polygons for gun turret lower part.

#### Declarations of makeBody():
```java
vector v[]
body = new polygon3D[5]
```

* These Declarations Construct polygons for this model.


```java
private void makeTurret()
```

* This method is responsible for create polygons for gun turret upper part.

```java
public void uptade()
```

* This method is responsible for upgrading the turret in the game scenario according to the actions in the game.

```java
private void processAI()
```

* This method has the function to calculate the distance between the tanks of the player and enemies , and also invoke enemy tanks next.

```java
public void draw()
```

* This method is responsible for draw the body of turret , and draw the smoke when attacked.

```java
public rectangle2D getBoundary2D()
```

* This method is responsible for return the limits of the explosion.

```java
public void damage(int damagePoint)
```

* This method intended to withdraw when the turret attacked life points, and its input parameter the value of the damage.

## Declarations:

```java
private polygon3D body [ ]
```

* Polygons for gunTurret body.

```java
private polygon3D turret [ ]
```

* Polygons for tank turret.

```java
private polygon3D shadowBody
```

* The shadow of tank body.

```java
private polygon3D shadowTurret
```

* The shadow of tank turret.

```java
private Vector bodyCenter
```

* The body focuses in the coordinate of the camera.

```java  
private Vector turretCenter
```

* The turret center (pivot point for rotation).

```java
private int turretAngle
```

* Total angle that the turret has rotated from the initial position. (in the x-z plane).

```java
private int targetAngle
```

* The target angle with respect to body center.

```java
private int turretAngleDelta
```

* Degrees the  gun turret has rotated in a frame.

```java
private boolean aimRight
```

* GunTurret moves to the Right.

```java
private boolean aimLeft
```

* GunTurret moves to the left.

```java
private boolean firing
```

* GunTurret shoot.

```java
private int coolDown
```

* Time needed before a weapon can be fired again.

```java
private int currentCoolDown
```

* Current coolDown.

```java
private int position
```

* The position index of the turret  in the grid map.

```java
private Smoke Smoke
```

* A smoke tail.

```java
private boolean isVisiblePreviousFrame
```

* Whether the gun turret is visible in the previous frame.

```java
private Vector tempVector1
```

* Temporary vector which will be used for vector arithmetic.

```java
private Vector tempVector2
```

* Temporary vectors which will be used for vector arithmetic.

```java
private boolean engaged
```

* An AI flag  indicates whether it has engaged with player tank

```java
private double distance
```

* Distance from player tank.

```java
private boolean clearToShoot
```

* An AI flag indicates whether there is a type 2 obstacle between gunTurret and player tank.