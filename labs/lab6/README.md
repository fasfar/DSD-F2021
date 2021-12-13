# Lab 6
 The objective of lab 6 was to program the FPGA board to run a pong game through a VGA display. The board used a 5 kΩ potentiometer to send input signals corresponding to the bat’s movement, which was programmed using the adc_if module to convert the analog input into a 12-bit digital signal to move the bat on the display. 

## Modifications

### Bat_n_ball
In the new file, every time the game begins the horizontal speed of the ball increases upon hitting the bat as seen when adding the ball_x_motion variable into the loop. The variable hit_count and dtop_dbl_hit were added to the mball process in order to account the number of times the ball hits the bat and to prevent a double hit of the ball on the bat, respectively. Whenever the ball hits the bat, the width of the bat(bat_w) decreases by 1 pixel and the hit_count increases by 1.
The variable hit_count was added to store the hit count that would be displayed on the 7-segment display.
### Pong.vhd
A cnt variable is implemented to generate the timing signals as the ball hits the bat every time and causes the ball to move faster.


# Lab 3
The objective of lab 3 was to program the FPGA board to display a bouncing ball on a VGA monitor. 

##Modifications
 ### In the new ball_1 file, the if statement in the bdraw process is rewritten into an equation for a circle taking into account the pixel columns and rows(pixel_col & pixel_row) and the position of the ball(ball_x & ball_y) which will allow for the ball to be circular instead of a square and a specific size. The signal variable ball_x_motion was also incorporated to allow the ball to move horizontally in addition to moving vertically. We also set the red and blue to 1 to allow only those colors to show which changed the color of the ball to purple.