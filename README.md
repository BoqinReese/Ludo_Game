# Ludo_Game
A game of Ludo written in python and pygame
import pygame, sys, time
from pygame.locals import*

pygame.init()
game_window = pygame.display.set_mode((900, 700))
pygame.display.set_caption('Ludo Slayers')

WHITE = (255, 255, 255)
RED = (255, 0 , 0)
GREEN = (0, 255, 0)
BLUE = (20,150,229)
YELLOW = (255, 255, 0)
BLACK = (0, 0, 0)
MAGENTA = (255, 0, 255)
game_window.fill(WHITE)

# Main board square
board_square = pygame.draw.rect(game_window, BLACK, (200, 10, 600, 600), 5)

# Inner squares
square1 = pygame.draw.rect(game_window, RED, (board_square.x, board_square.y+1, 200, 200))
square1
square2 = pygame.draw.rect(game_window, BLUE, (600, board_square.y+1, 200, 200))
square2
square3 = pygame.draw.rect(game_window, GREEN, (board_square.x, 410, 200, 200))
square3
square4 = pygame.draw.rect(game_window, YELLOW, (600, 410, 200, 200))
square4
center_square = pygame.draw.rect(game_window, BLACK, (square1.right, square1.bottom, 200, 200), 3)

# Inner Circles of first square going clock-wise...
# Each inner circle with its coin...
# First Square
square1_circle1 = pygame.draw.circle(game_window, WHITE, (250, 60), 33)
square1_circle1_coin = pygame.draw.circle(game_window, RED, (square1_circle1.centerx, square1_circle1.centery), 20)
square1_circle1 = pygame.draw.circle(game_window, BLACK, (250, 60), 33, 3)

square1_circle2 = pygame.draw.circle(game_window, WHITE, (350, 60), 33)
square1_circle2_coin = pygame.draw.circle(game_window, RED, (square1_circle2.centerx, square1_circle2.centery), 20)
square1_circle2 = pygame.draw.circle(game_window, BLACK, (350, 60), 33, 3)

square1_circle3 = pygame.draw.circle(game_window, WHITE, (250, 160), 33)
square1_circle3_coin = pygame.draw.circle(game_window, RED, (square1_circle3.centerx, square1_circle3.centery), 20)
square1_circle3 = pygame.draw.circle(game_window, BLACK, (250, 160), 33, 3)

square1_circle4 = pygame.draw.circle(game_window, WHITE, (350, 160), 33)
square1_circle4_coin = pygame.draw.circle(game_window, RED, (square1_circle4.centerx, square1_circle4.centery), 20)
square1_circle4 = pygame.draw.circle(game_window, BLACK, (350, 160), 33, 3)

# Second Square
square2_circle1 = pygame.draw.circle(game_window, WHITE, (650, 60), 33)
square2_circle1_coin = pygame.draw.circle(game_window, BLUE, (square2_circle1.centerx, square2_circle1.centery), 20)
square2_circle1 = pygame.draw.circle(game_window, BLACK, (650, 60), 33, 3)

square2_circle2 = pygame.draw.circle(game_window, WHITE, (750, 60), 33)
square2_circle2_coin = pygame.draw.circle(game_window, BLUE, (square2_circle2.centerx, square2_circle2.centery), 20)
square2_circle2 = pygame.draw.circle(game_window, BLACK, (750, 60), 33, 3)

square2_circle3 = pygame.draw.circle(game_window, WHITE, (650, 160), 33)
square2_circle3_coin = pygame.draw.circle(game_window, BLUE, (square2_circle3.centerx, square2_circle3.centery), 20)
square2_circle3 = pygame.draw.circle(game_window, BLACK, (650, 160), 33, 3)

square2_circle4 = pygame.draw.circle(game_window, WHITE, (750, 160), 33)
square2_circle4_coin = pygame.draw.circle(game_window, BLUE, (square2_circle4.centerx, square2_circle4.centery), 20)
square2_circle4 = pygame.draw.circle(game_window, BLACK, (750, 160), 33, 3)

# Third Square
square3_circle1 = pygame.draw.circle(game_window, WHITE, (250, 460), 33)
square3_circle1_coin = pygame.draw.circle(game_window, GREEN, (square3_circle1.centerx, square3_circle1.centery), 20)
square3_circle1 = pygame.draw.circle(game_window, BLACK, (250, 460), 33, 3)

square3_circle2 = pygame.draw.circle(game_window, WHITE, (350, 460), 33)
square3_circle2_coin = pygame.draw.circle(game_window, GREEN, (square3_circle2.centerx, square3_circle2.centery), 20)
square3_circle2 = pygame.draw.circle(game_window, BLACK, (350, 460), 33, 3)

square3_circle3 = pygame.draw.circle(game_window, WHITE, (250, 560), 33)
square3_circle3_coin = pygame.draw.circle(game_window, GREEN, (square3_circle3.centerx, square3_circle3.centery), 20)
square3_circle3 = pygame.draw.circle(game_window, BLACK, (250, 560), 33, 3)

square3_circle4 = pygame.draw.circle(game_window, WHITE, (350, 560), 33)
square3_circle4_coin = pygame.draw.circle(game_window, GREEN, (square3_circle4.centerx, square3_circle4.centery), 20)
square3_circle4 = pygame.draw.circle(game_window, BLACK, (350, 560), 33, 3)


# Fourth Square
square4_circle1 = pygame.draw.circle(game_window, WHITE, (650, 460), 33)
square4_circle1_coin = pygame.draw.circle(game_window, YELLOW, (square4_circle1.centerx, square4_circle1.centery), 20)
square4_circle1 = pygame.draw.circle(game_window, BLACK, (650, 460), 33, 3)

square4_circle2 = pygame.draw.circle(game_window, WHITE, (750, 460), 33)
square4_circle2_coin = pygame.draw.circle(game_window, YELLOW, (square4_circle2.centerx, square4_circle2.centery), 20)
square4_circle2 = pygame.draw.circle(game_window, BLACK, (750, 460), 33, 3)

square4_circle3 = pygame.draw.circle(game_window, WHITE, (650, 560), 33)
square4_circle3_coin = pygame.draw.circle(game_window, YELLOW, (square4_circle3.centerx, square4_circle3.centery), 20)
square4_circle3 = pygame.draw.circle(game_window, BLACK, (650, 560), 33, 3)

square4_circle4 = pygame.draw.circle(game_window, WHITE, (750, 560), 33)
square4_circle4_coin = pygame.draw.circle(game_window, YELLOW, (square4_circle4.centerx, square4_circle4.centery), 20)
square4_circle4 = pygame.draw.circle(game_window, BLACK, (750, 560), 33, 3)


# Drawing the cells
# But first inner lines
# center left
pygame.draw.line(game_window, BLACK, (square1.x, square1.bottom + 66.7), (square1.right, square1.bottom + 66.7), 2)
pygame.draw.line(game_window, BLACK, (square1.x, square1.bottom + 133.4), (square1.right, square1.bottom + 133.4), 2)
# center right
pygame.draw.line(game_window, BLACK, (square2.x, square2.bottom + 66.7), (square2.right, square2.bottom + 66.7), 2)
pygame.draw.line(game_window, BLACK, (square2.x, square2.bottom + 133.4), (square2.right, square2.bottom + 133.4), 2)
# center top
pygame.draw.line(game_window, BLACK, (square1.right + 66.7, square1.y), (square1.right + 66.7, square1.bottom), 2)
pygame.draw.line(game_window, BLACK, (square1.right + 133.4, square1.y), (square1.right + 133.4, square1.bottom), 2)
# center bottom
pygame.draw.line(game_window, BLACK, (square3.right + 66.7, square3.y), (square3.right + 66.7, square3.bottom), 2)
pygame.draw.line(game_window, BLACK, (square3.right + 133.4, square3.y), (square3.right + 133.4, square3.bottom), 2)

# Now the cells
#top_center_left cells
tcl_cell1 = pygame.draw.rect(game_window, BLACK, (board_square.x-1, square1.bottom, 34, 68), 1)
tcl_cell2 = pygame.draw.rect(game_window, RED, (board_square.x-1 + 34, square1.bottom, 34, 68),)
tcl_cell2 = pygame.draw.rect(game_window, BLACK, (board_square.x-1 + 34, square1.bottom, 34, 68), 1)
tcl_cell3 = pygame.draw.rect(game_window, BLACK, (board_square.x-1 + 68, square1.bottom, 34, 68), 1)
tcl_cell4 = pygame.draw.rect(game_window, BLACK, (board_square.x-1 + 102, square1.bottom, 34, 68), 1)
tcl_cell5 = pygame.draw.rect(game_window, BLACK, (board_square.x-1 + 136, square1.bottom, 34, 68), 1)
tcl_cell6 = pygame.draw.rect(game_window, BLACK, (board_square.x-1 + 170, square1.bottom, 34, 68), 1)

#mid_center_left cells
mcl_cell1 = pygame.draw.rect(game_window, BLACK, (board_square.x-1, tcl_cell1.bottom, 34, 68), 1)
mcl_cell2 = pygame.draw.rect(game_window, RED, (board_square.x-1 + 34, tcl_cell2.bottom, 34, 68)) #Color
mcl_cell2 = pygame.draw.rect(game_window, BLACK, (board_square.x-1 + 34, tcl_cell2.bottom, 34, 68), 1)
mcl_cell3 = pygame.draw.rect(game_window, RED, (board_square.x-1 + 68, tcl_cell2.bottom, 34, 68)) # Color
mcl_cell3 = pygame.draw.rect(game_window, BLACK, (board_square.x-1 + 68, tcl_cell3.bottom, 34, 68), 1)
mcl_cell4 = pygame.draw.rect(game_window, RED, (board_square.x-1 + 102, tcl_cell2.bottom, 34, 68)) # Color
mcl_cell4 = pygame.draw.rect(game_window, BLACK, (board_square.x-1 + 102, tcl_cell4.bottom, 34, 68), 1)
mcl_cell5 = pygame.draw.rect(game_window, RED, (board_square.x-1 + 136, tcl_cell2.bottom, 34, 68)) # Color
mcl_cell5 = pygame.draw.rect(game_window, BLACK, (board_square.x-1 + 136, tcl_cell5.bottom, 34, 68), 1)
mcl_cell6 = pygame.draw.rect(game_window, RED, (board_square.x-1 + 170, tcl_cell2.bottom, 34, 68)) # Color
mcl_cell6 = pygame.draw.rect(game_window, BLACK, (board_square.x-1 + 170, tcl_cell6.bottom, 34, 68), 1)

#lower_center_left cells
lcl_cell1 = pygame.draw.rect(game_window, BLACK, (board_square.x-1, mcl_cell1.bottom-2, 34, 68), 1)
lcl_cell2 = pygame.draw.rect(game_window, BLACK, (board_square.x-1 + 34, mcl_cell2.bottom-2, 34, 68), 1)
lcl_cell3 = pygame.draw.rect(game_window, BLACK, (board_square.x-1 + 68, mcl_cell3.bottom-2, 34, 68), 1)
lcl_cell4 = pygame.draw.rect(game_window, BLACK, (board_square.x-1 + 102, mcl_cell4.bottom-2, 34, 68), 1)
lcl_cell5 = pygame.draw.rect(game_window, BLACK, (board_square.x-1 + 136, mcl_cell5.bottom-2, 34, 68), 1)
lcl_cell6 = pygame.draw.rect(game_window, BLACK, (board_square.x-1 + 170, mcl_cell6.bottom-2, 34, 68), 1)



#left_center_top cells
lct_cell1 = pygame.draw.rect(game_window, BLACK, (square1.right, square1.y-1, 68, 34), 1)
lct_cell2 = pygame.draw.rect(game_window, BLACK, (square1.right, square1.y-1 + 34, 68, 34), 1)
lct_cell3 = pygame.draw.rect(game_window, BLACK, (square1.right, square1.y-1 + 68, 68, 34), 1)
lct_cell4 = pygame.draw.rect(game_window, BLACK, (square1.right, square1.y-1 + 102, 68, 34), 1)
lct_cell5 = pygame.draw.rect(game_window, BLACK, (square1.right, square1.y-1 + 136, 68, 34), 1)
lct_cell6 = pygame.draw.rect(game_window, BLACK, (square1.right, square1.y-1 + 170, 68, 34), 1)

#mid_center_top cells
mct_cell1 = pygame.draw.rect(game_window, BLACK, (lct_cell1.right, lct_cell1.y, 68, 34), 1)
mct_cell2 = pygame.draw.rect(game_window, BLUE, (lct_cell2.right, lct_cell2.y, 68, 34))
mct_cell2 = pygame.draw.rect(game_window, BLACK, (lct_cell2.right, lct_cell2.y, 68, 34), 1)
mct_cell3 = pygame.draw.rect(game_window, BLUE, (lct_cell3.right, lct_cell3.y, 68, 34))
mct_cell3 = pygame.draw.rect(game_window, BLACK, (lct_cell3.right, lct_cell3.y, 68, 34), 1)
mct_cell4 = pygame.draw.rect(game_window, BLUE, (lct_cell4.right, lct_cell4.y, 68, 34))
mct_cell4 = pygame.draw.rect(game_window, BLACK, (lct_cell4.right, lct_cell4.y, 68, 34), 1)
mct_cell5 = pygame.draw.rect(game_window, BLUE, (lct_cell5.right, lct_cell5.y, 68, 34))
mct_cell5 = pygame.draw.rect(game_window, BLACK, (lct_cell5.right, lct_cell5.y, 68, 34), 1)
mct_cell6 = pygame.draw.rect(game_window, BLUE, (lct_cell6.right, lct_cell6.y, 68, 34))
mct_cell6 = pygame.draw.rect(game_window, BLACK, (lct_cell6.right, lct_cell6.y, 68, 34), 1)

#right_center_top cells
rct_cell1 = pygame.draw.rect(game_window, BLACK, (mct_cell1.right-2, mct_cell1.y, 68, 34), 1)
rct_cell2 = pygame.draw.rect(game_window, BLUE, (mct_cell2.right-2, mct_cell2.y, 68, 34))
rct_cell2 = pygame.draw.rect(game_window, BLACK, (mct_cell2.right-2, mct_cell2.y, 68, 34), 1)
rct_cell3 = pygame.draw.rect(game_window, BLACK, (mct_cell3.right-2, mct_cell3.y, 68, 34), 1)
rct_cell4 = pygame.draw.rect(game_window, BLACK, (mct_cell4.right-2, mct_cell4.y, 68, 34), 1)
rct_cell5 = pygame.draw.rect(game_window, BLACK, (mct_cell5.right-2, mct_cell5.y, 68, 34), 1)
rct_cell6 = pygame.draw.rect(game_window, BLACK, (mct_cell6.right-2, mct_cell6.y, 68, 34), 1)



#Top_center_right cells
tcr_cell1 = pygame.draw.rect(game_window, BLACK, (board_square.right - 34, square2.bottom-1, 34, 68), 1)
tcr_cell2 = pygame.draw.rect(game_window, BLACK, (board_square.right - 68, square1.bottom-1, 34, 68), 1)
tcr_cell3 = pygame.draw.rect(game_window, BLACK, (board_square.right - 102, square1.bottom-1, 34, 68), 1)
tcr_cell4 = pygame.draw.rect(game_window, BLACK, (board_square.right - 136, square1.bottom-1, 34, 68), 1)
tcr_cell5 = pygame.draw.rect(game_window, BLACK, (board_square.right - 170, square1.bottom-1, 34, 68), 1)
tcr_cell6 = pygame.draw.rect(game_window, BLACK, (board_square.right - 204, square1.bottom-1, 34, 68), 1)

#mid_center_right cells
mcr_cell1 = pygame.draw.rect(game_window, BLACK, (board_square.right - 34, tcr_cell1.bottom-1, 34, 68), 1)
mcr_cell2 = pygame.draw.rect(game_window, YELLOW, (board_square.right - 68, tcr_cell2.bottom-1, 34, 68))
mcr_cell2 = pygame.draw.rect(game_window, BLACK, (board_square.right - 68, tcr_cell2.bottom-1, 34, 68), 1)
mcr_cell3 = pygame.draw.rect(game_window, YELLOW, (board_square.right - 102, tcr_cell3.bottom-1, 34, 68))
mcr_cell3 = pygame.draw.rect(game_window, BLACK, (board_square.right - 102, tcr_cell3.bottom-1, 34, 68), 1)
mcr_cell4 = pygame.draw.rect(game_window, YELLOW, (board_square.right - 136, tcr_cell4.bottom-1, 34, 68))
mcr_cell4 = pygame.draw.rect(game_window, BLACK, (board_square.right - 136, tcr_cell4.bottom-1, 34, 68), 1)
mcr_cell5 = pygame.draw.rect(game_window, YELLOW, (board_square.right - 170, tcr_cell5.bottom-1, 34, 68))
mcr_cell5 = pygame.draw.rect(game_window, BLACK, (board_square.right - 170, tcr_cell5.bottom-1, 34, 68), 1)
mcr_cell6 = pygame.draw.rect(game_window, YELLOW, (board_square.right - 204, tcr_cell6.bottom-1, 34, 68))
mcr_cell6 = pygame.draw.rect(game_window, BLACK, (board_square.right - 204, tcr_cell6.bottom-1, 34, 68), 1)

#lower_center_right cells
lcr_cell1 = pygame.draw.rect(game_window, BLACK, (board_square.right - 34, mcr_cell1.bottom-1, 34, 68), 1)
lcr_cell2 = pygame.draw.rect(game_window, YELLOW, (board_square.right - 68, mcr_cell2.bottom-1, 34, 68))
lcr_cell2 = pygame.draw.rect(game_window, BLACK, (board_square.right - 68, mcr_cell2.bottom-1, 34, 68), 1)
lcr_cell3 = pygame.draw.rect(game_window, BLACK, (board_square.right - 102, mcr_cell3.bottom-1, 34, 68), 1)
lcr_cell4 = pygame.draw.rect(game_window, BLACK, (board_square.right - 136, mcr_cell4.bottom-1, 34, 68), 1)
lcr_cell5 = pygame.draw.rect(game_window, BLACK, (board_square.right - 170, mcr_cell5.bottom-1, 34, 68), 1)
lcr_cell6 = pygame.draw.rect(game_window, BLACK, (board_square.right - 204, mcr_cell6.bottom-1, 34, 68), 1)


#Left center_bottom
lcb_cell1 = pygame.draw.rect(game_window, BLACK, (square3.right, square3.y-2, 68, 34), 1)
lcb_cell2 = pygame.draw.rect(game_window, BLACK, (square3.right, square3.y-2 + 34, 68, 34), 1)
lcb_cell3 = pygame.draw.rect(game_window, BLACK, (square3.right, square3.y-2 + 68, 68, 34), 1)
lcb_cell4 = pygame.draw.rect(game_window, BLACK, (square3.right, square3.y-2 + 102, 68, 34), 1)
lcb_cell5 = pygame.draw.rect(game_window, GREEN, (square3.right, square3.y-2 + 136, 68, 34))
lcb_cell5 = pygame.draw.rect(game_window, BLACK, (square3.right, square3.y-2 + 136, 68, 34), 1)
lcb_cell6 = pygame.draw.rect(game_window, BLACK, (square3.right, square3.y-2 + 170, 68, 34), 1)

#mid_center_bottom cells
mcb_cell1 = pygame.draw.rect(game_window, GREEN, (lcb_cell1.right, lcb_cell1.y, 68, 34))
mcb_cell1 = pygame.draw.rect(game_window, BLACK, (lcb_cell1.right, lcb_cell1.y, 68, 34), 1)
mcb_cell2 = pygame.draw.rect(game_window, GREEN, (lcb_cell2.right, lcb_cell2.y, 68, 34))
mcb_cell2 = pygame.draw.rect(game_window, BLACK, (lcb_cell2.right, lcb_cell2.y, 68, 34), 1)
mcb_cell3 = pygame.draw.rect(game_window, GREEN, (lcb_cell3.right, lcb_cell3.y, 68, 34))
mcb_cell3 = pygame.draw.rect(game_window, BLACK, (lcb_cell3.right, lcb_cell3.y, 68, 34), 1)
mcb_cell4 = pygame.draw.rect(game_window, GREEN, (lcb_cell4.right, lcb_cell4.y, 68, 34))
mcb_cell4 = pygame.draw.rect(game_window, BLACK, (lcb_cell4.right, lcb_cell4.y, 68, 34), 1)
mcb_cell5 = pygame.draw.rect(game_window, GREEN, (lcb_cell5.right, lcb_cell5.y, 68, 34))
mcb_cell5 = pygame.draw.rect(game_window, BLACK, (lcb_cell5.right, lcb_cell5.y, 68, 34), 1)
mcb_cell6 = pygame.draw.rect(game_window, BLACK, (lcb_cell6.right, lcb_cell6.y, 68, 34), 1)

#right_center_bottom cells
rcb_cell1 = pygame.draw.rect(game_window, BLACK, (mcb_cell1.right-2, mcb_cell1.y, 68, 34), 1)
rcb_cell2 = pygame.draw.rect(game_window, BLACK, (mcb_cell2.right-2, mcb_cell2.y, 68, 34), 1)
rcb_cell3 = pygame.draw.rect(game_window, BLACK, (mcb_cell3.right-2, mcb_cell3.y, 68, 34), 1)
rcb_cell4 = pygame.draw.rect(game_window, BLACK, (mcb_cell4.right-2, mcb_cell4.y, 68, 34), 1)
rcb_cell5 = pygame.draw.rect(game_window, BLACK, (mcb_cell5.right-2, mcb_cell5.y, 68, 34), 1)
rcb_cell6 = pygame.draw.rect(game_window, BLACK, (mcb_cell6.right-2, mcb_cell6.y, 68, 34), 1)

# The center Triangles
pygame.draw.polygon(game_window, YELLOW, ((center_square.centerx, center_square.centery), (center_square.x + 200, center_square.y),(center_square.x + 200, center_square.y + 200)))
pygame.draw.polygon(game_window, RED, ((center_square.centerx, center_square.centery), (center_square.x, center_square.y),(center_square.x, center_square.y + 200)))
pygame.draw.polygon(game_window, BLUE, ((center_square.centerx, center_square.centery), (center_square.x , center_square.y),(center_square.x + 200, center_square.y)))
pygame.draw.polygon(game_window, GREEN, ((center_square.centerx, center_square.centery), (center_square.x, center_square.y + 200),(center_square.x + 200, center_square.y + 200)))
pygame.draw.rect(game_window, BLACK, (square1.right, square1.bottom, 200, 200), 3) # Center square frame
# center square cross lines
pygame.draw.line(game_window, BLACK, (center_square.x-1, center_square.y), (center_square.x + 200, center_square.y + 200), 2)
pygame.draw.line(game_window, BLACK, (center_square.x + 200, center_square.y), (center_square.x, center_square.y + 200), 2)


# The side pane

# Vertical Line
pygame.draw.line(game_window, ((220,220,220)), (180, 0), (180, 700), 4)
# Horizontal Line
pygame.draw.line(game_window, ((220,220,220)), (0, 450), (180, 450), 4)


# Text Box
the_font = pygame.font.SysFont('Agency FB', 40)
pygame.draw.rect(game_window, RED, (20, 160, 60, 60))

# Start Button
#def start_button():
start_button1 = pygame.draw.rect(game_window, GREEN, (16, 643, 100, 40))
start_button2 = pygame.draw.rect(game_window, BLACK, (16, 643, 100, 40), 3)
start = the_font.render('START', 1, WHITE)
game_window.blit(start, (20, 650))
#pause_button1 = pygame.draw.rect(game_window, MAGENTA, (16, 643, 100, 40))

def pause_button():
    pause_button1 = pygame.draw.rect(game_window, RED, (16, 643, 100, 40))
    pause_button2 = pygame.draw.rect(game_window, BLACK, (16, 643, 100, 40), 3)
    game_window.blit(pause, (20, 650))

def proceed_button():
    pygame.draw.rect(game_window, MAGENTA, (16, 643, 100, 40))
    pygame.draw.rect(game_window, BLACK, (16, 643, 100, 40), 3)
    game_window.blit(proceed, (20, 650))



class ChooseColor():
	''' Pick a color to start playing...'''
	def __init__(self):

		'''Initiate'''

	def choose_color(self):
		select_color = the_font.render('Choose a color...', 1, BLACK)
		game_window.blit(select_color, (200, 650))

	def red_color(self):
		red_color_box = pygame.draw.rect(game_window, BLACK, (450, 620, 60, 60), 3)
		return pygame.draw.rect(game_window, RED, (450, 620, 60, 60))

	def blue_color(self):
		blue_color_box = pygame.draw.rect(game_window, BLACK, (550, 620, 60, 60), 3)
		return pygame.draw.rect(game_window, BLUE, (550, 620, 60, 60))

	def yellow_color(self):
		yellow_color_box = pygame.draw.rect(game_window, BLACK, (650, 620, 60, 60), 3)
		return pygame.draw.rect(game_window, YELLOW, (650, 620, 60, 60))

	def green_color(self):
		green_color_box = pygame.draw.rect(game_window, BLACK, (750, 620, 60, 60), 3)
		return pygame.draw.rect(game_window, GREEN, (750, 620, 60, 60))



	'''def color_boxes(self):
		red_color_box = pygame.draw.rect(game_window, BLACK, (450, 620, 60, 60), 3)
		blue_color_box = pygame.draw.rect(game_window, BLACK, (550, 620, 60, 60), 3)
		yellow_color_box = pygame.draw.rect(game_window, BLACK, (650, 620, 60, 60), 3)
		green_color_box = pygame.draw.rect(game_window, BLACK, (750, 620, 60, 60), 3)'''


choose_color = ChooseColor()

# Dice
def dice_sides():
    if roll_dice == 1:
        side1 = pygame.draw.rect(game_window, RED, (20, 300, 60, 60))
        pygame.draw.circle(game_window, WHITE, (side1.centerx, side1.centery), 10)
    elif roll_dice == 2:
        side2 = pygame.draw.rect(game_window, RED, (20, 300, 60, 60))
        pygame.draw.circle(game_window, WHITE, (side2.x+20, side2.y+30), 8)
        pygame.draw.circle(game_window, WHITE, (side2.x+40, side2.y+30), 8)
    elif roll_dice == 3:
        side3 = pygame.draw.rect(game_window, RED, (20, 300, 60, 60))
        pygame.draw.circle(game_window, WHITE, (side3.x+10, side3.y+30), 8)
        pygame.draw.circle(game_window, WHITE, (side3.x+30, side3.y+30), 8)
        pygame.draw.circle(game_window, WHITE, (side3.x+50, side3.y+30), 8)
    elif roll_dice == 4:
        side4 = pygame.draw.rect(game_window, RED, (20, 300, 60, 60))
        pygame.draw.circle(game_window, WHITE, (side4.x+20, side4.y+20), 8)
        pygame.draw.circle(game_window, WHITE, (side4.x+40, side4.y+20), 8)
        pygame.draw.circle(game_window, WHITE, (side4.x+20, side4.y+40), 8)
        pygame.draw.circle(game_window, WHITE, (side4.x+40, side4.y+40), 8)
    elif roll_dice == 5:
        side5 = pygame.draw.rect(game_window, RED, (20, 300, 60, 60))
        pygame.draw.circle(game_window, WHITE, (side5.x+15, side5.y+15), 8)
        pygame.draw.circle(game_window, WHITE, (side5.x+45, side5.y+15), 8)
        pygame.draw.circle(game_window, WHITE, (side5.x+30, side5.y+30), 8)
        pygame.draw.circle(game_window, WHITE, (side5.x+15, side5.y+45), 8)
        pygame.draw.circle(game_window, WHITE, (side5.x+45, side5.y+45), 8)
    elif roll_dice == 6:
        side6 = pygame.draw.rect(game_window, RED, (20, 300, 60, 60))
        pygame.draw.circle(game_window, WHITE, (side6.x+18, side6.y+10), 8)
        pygame.draw.circle(game_window, WHITE, (side6.x+18, side6.y+30), 8)
        pygame.draw.circle(game_window, WHITE, (side6.x+18, side6.y+50), 8)
        pygame.draw.circle(game_window, WHITE, (side6.x+42, side6.y+10), 8)
        pygame.draw.circle(game_window, WHITE, (side6.x+42, side6.y+30), 8)
        pygame.draw.circle(game_window, WHITE, (side6.x+42, side6.y+50), 8)



# And now the main game logic begins...


def first_attempt():
    roll_dice = random.randint(1,6)
    dice_sides()
    if roll_dice != 6:
        print('First attempt failed, Try again..')
        print('Rolling again..')
        roll_dice = random.randint(1,6)
    else:
    	dice_sides




#Main game Loop
while True:
    for event in pygame.event.get():
        if event.type == QUIT:
            pygame.quit()
            sys.exit()

        if event.type == pygame.MOUSEBUTTONDOWN:
            mouse_x, mouse_y = pygame.mouse.get_pos()
            if start_button1.collidepoint(mouse_x, mouse_y):
                start = the_font.render('START', 1, RED)
                pause_button()
                time.sleep(1)
                choose_color.choose_color()
                choose_color.red_color()
                #choose_color.color_boxes()
                
            if choose_color.red_color().collidepoint(mouse_x, mouse_y):
            	pygame.draw.rect(game_window, WHITE, (200, 615, 650, 100))
            	game_window.blit(red_turn, (200, 650))
            	#time.sleep(2)
            	# Start coding the individual color logic.....
            	#color_red()
            	'''
            if choose_color.blue_color().collidepoint(mouse_x, mouse_y):
            	pygame.draw.rect(game_window, WHITE, (200, 615, 650, 100))
            	game_window.blit(blue_turn, (200, 650))
            	# color_blue()

            if choose_color.yellow_color().collidepoint(mouse_x, mouse_y):
                pygame.draw.rect(game_window, WHITE, (200, 615, 650, 100))
                game_window.blit(yellow_turn, (200, 650))
                # yellow_color()

            if choose_color.green_color().collidepoint(mouse_x, mouse_y):
                pygame.draw.rect(game_window, WHITE, (200, 615, 650, 100))
                game_window.blit(green_turn, (200, 650))
                # green_color()
            #else:
            #	pygame.draw.rect(game_window, WHITE, (200, 615, 650, 100))'''


    scores_label = the_font.render('SCORE', 1, GREEN)
    real_scores = the_font.render('0', 1, BLUE)
    next_color = the_font.render('NEXT', 1, GREEN)
    dice = the_font.render('DICE', 1, GREEN)
    hints = the_font.render('HINTS', 1, GREEN)
    pause = the_font.render('PAUSE', 1, WHITE)
    proceed = the_font.render('PROCEED', 1, WHITE)
    red_turn = the_font.render('Red is playing..', 1, BLACK)
    blue_turn = the_font.render('Red will play first..', 1, BLACK)
    yellow_turn = the_font.render('Red will play first..', 1, BLACK)
    green_turn = the_font.render('Red will play first..', 1, BLACK)
    game_window.blit(scores_label, (20, 30))
    game_window.blit(real_scores, (20, 60))
    game_window.blit(next_color, (20, 130))
    game_window.blit(dice, (20, 250))
    game_window.blit(hints, (20, 420))
    pygame.display.flip()
