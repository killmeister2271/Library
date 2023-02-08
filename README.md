# Library
Coding is fun! Why not make it easy too? [ALWAYS WIP]

vector is set up as follows:

vector.g2D(<number>,<number>)

The children of the vector are as follows:
X, Y, dist, rot, dir, dirOwner, doMath, addEventListener, removeEventListener
  
distance is Math.sqrt((X**2)+(Y**2))
rot is what angle the vector is going from 0, 0 in degrees
dir is the direction it's facing. it is also a vector object
dirOwner is either null if you are accessing it from the vector itself OR the original vector if you are looking from the dir
doMath is a function with 3 parameters. the first parameter is either "+", "-", "*" or "/", the 2nd is the X value, and the 3rd is the Y value.

create.part is set up as follows:

create.part({
  tagName: <HTMLElement tag>,
  Parent: <where the HTMLElement will be stored>,
  Position: <vector>,
  Size: <vector>,
  Rotation: <number of degrees>,
  Color: <something the style of the element would recognize as a color. I prefer hexadecimal values>,
  Customization: <a function with 1 parameter which is the actual HTMLElement>
})

Once you have the "part" created, you can get the actual HTMLElement of it this way:
 var foo = create.part(blah blah blah); var bar = foo.rawPart;

There is also this useful tidbit of information:
 bar.cookedPart===foo
  
getHitbox is a function with 3 parameters: Position, Size, and Rotation. With this, you know exactly the hitbox of a square.
