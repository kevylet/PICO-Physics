# PICO-Physics

// Initial implementation
OBB Object Implementation - Quin
- An object with:
  - cx
  - cy
  - x1
  - y1
  - v1_x
  - v1_y
  - x2
  - y2
  - v2_x
  - v2_y
  - x3
  - y3
  - v3_x
  - v3_y
  - x4
  - y4
  - v4_x
  - v4_y
  - movable
  
Collision Detection - Jake
- Detect collision between boxes
- Change velocity depending on collisions

Linear Transforms (Gravity) - Kevin
- Move boxes every frame based on their velocity

Draw All Boxes -Brandon
- Loop through the world table, drawing lines between each of the boxes' points

// Second implementation
Improve collision to use SAT
 - Try to find axis between boxes
 - True if no axis, false if axis exists

Implement next-frame collision check
 - Run collision checks on the next frame using each box's current velocities
 
 Add rotation function - Kevin
 - Rotate a box by a specified angle around its center point
 - Usage: rotate_box(box, angle)
 
 Determine when a box should fall & rotate
  - Find out when a box's center point if over the edge of the box below it
  - Determine a ratio of rotation based on how far off the edge the center point is
  - Apply a rotation to the box using rotate_box() that is the ratio multiplied against a constant (ROT_FACTOR)
