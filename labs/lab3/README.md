# Lab 3
The objective of lab 3 was to program the FPGA board to display a bouncing ball on a VGA monitor. 

##Modifications
 
### In the new ball_1 file, the if statement in the bdraw process is rewritten into an equation for a circle taking into account the pixel columns and rows(pixel_col & pixel_row) and the position of the ball(ball_x & ball_y) which will allow for the ball to be circular instead of a square and a specific size. The signal variable ball_x_motion was also incorporated to allow the ball to move horizontally in addition to moving vertically. We also set the red and blue to 1 to allow only those colors to show which changed the color of the ball to purple.