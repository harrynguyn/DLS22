from pytesseract import pytesseract
import pyautogui as pg
from tkinter import *
import numpy as np
import datetime
import time
import cv2

root=Tk()
root.title('Binocchoa')
root.geometry("200x200")
button_frame=Frame(root).pack(side=BOTTOM)
def tool():
	while True:
		try:
			pg.screenshot('scr.png')
		except:
			print("Bonk")
		now = datetime.datetime.now()
		scr = cv2.imread('scr.png')# main pic

		ok = cv2.imread('OK.png')
		con = cv2.imread('continue.png')
		DLS22 = cv2.imread('DLS22.png')
		play = cv2.imread('Play.png')
		playing = cv2.imread('Playing.png')
		read = cv2.imread('Read.png')
		x = cv2.imread('x.png')
		xp = cv2.imread('XP.png')
		url = cv2.imread('url.png')
		home = cv2.imread('home.png')
		cancel = cv2.imread('cancel.png')
		dls = cv2.imread('dls.png')
		mall = cv2.imread('mall.png')
		ch = cv2.imread('ch.png')
		back = cv2.imread('back.png')
		fix = cv2.imread('fix.png')
		tw = cv2.imread('tw.png')
		twu = cv2.imread('twu.png')
		load = cv2.imread('reload.png')
		cc = cv2.imread('cc.png')
		cc1 = cv2.imread('cc1.png')
		cc2 = cv2.imread('cc2.png')
		cc3 = cv2.imread('cc3.png')
		cc4 = cv2.imread('cc4.png')
		cc5 = cv2.imread('cc5.png')
		cc6 = cv2.imread('cc6.png')
		cc7 = cv2.imread('cc7.png')
		cc8 = cv2.imread('cc8.png')
		cc9 = cv2.imread('cc9.png')
		cc10 = cv2.imread('Kc.png')
		#sosanh 2 ảnh
		try:
			result_ok = cv2.matchTemplate(scr, ok, cv2.TM_CCOEFF_NORMED)
			result_con = cv2.matchTemplate(scr, con, cv2.TM_CCOEFF_NORMED)
			result_DLS22 = cv2.matchTemplate(scr, DLS22, cv2.TM_CCOEFF_NORMED)
			result_play = cv2.matchTemplate(scr, play, cv2.TM_CCOEFF_NORMED)
			result_playing = cv2.matchTemplate(scr, playing, cv2.TM_CCOEFF_NORMED)
			result_read = cv2.matchTemplate(scr, read, cv2.TM_CCOEFF_NORMED)
			result_x = cv2.matchTemplate(scr, x, cv2.TM_CCOEFF_NORMED)
			result_xp = cv2.matchTemplate(scr, xp, cv2.TM_CCOEFF_NORMED)
			result_url = cv2.matchTemplate(scr, url, cv2.TM_CCOEFF_NORMED)
			result_home = cv2.matchTemplate(scr, home, cv2.TM_CCOEFF_NORMED)
			result_cancel = cv2.matchTemplate(scr, cancel, cv2.TM_CCOEFF_NORMED)
			result_dls = cv2.matchTemplate(scr, dls, cv2.TM_CCOEFF_NORMED)
			result_mall = cv2.matchTemplate(scr, mall, cv2.TM_CCOEFF_NORMED)
			result_ch = cv2.matchTemplate(scr, ch, cv2.TM_CCOEFF_NORMED)
			result_fix = cv2.matchTemplate(scr, fix, cv2.TM_CCOEFF_NORMED)
			result_back = cv2.matchTemplate(scr, back, cv2.TM_CCOEFF_NORMED)
			result_tw = cv2.matchTemplate(scr, tw, cv2.TM_CCOEFF_NORMED)
			result_twu = cv2.matchTemplate(scr, twu, cv2.TM_CCOEFF_NORMED)
			result_load = cv2.matchTemplate(scr, load, cv2.TM_CCOEFF_NORMED)
			result_cc = cv2.matchTemplate(scr, cc, cv2.TM_CCOEFF_NORMED)
			result_cc1 = cv2.matchTemplate(scr, cc1, cv2.TM_CCOEFF_NORMED)
			result_cc2 = cv2.matchTemplate(scr, cc2, cv2.TM_CCOEFF_NORMED)
			result_cc3 = cv2.matchTemplate(scr, cc3, cv2.TM_CCOEFF_NORMED)
			result_cc4 = cv2.matchTemplate(scr, cc4, cv2.TM_CCOEFF_NORMED)
			result_cc5 = cv2.matchTemplate(scr, cc5, cv2.TM_CCOEFF_NORMED)
			result_cc6 = cv2.matchTemplate(scr, cc6, cv2.TM_CCOEFF_NORMED)
			result_cc7 = cv2.matchTemplate(scr, cc7, cv2.TM_CCOEFF_NORMED)
			result_cc8 = cv2.matchTemplate(scr, cc8, cv2.TM_CCOEFF_NORMED)
			result_cc9 = cv2.matchTemplate(scr, cc9, cv2.TM_CCOEFF_NORMED)
			result_cc10 = cv2.matchTemplate(scr, cc10, cv2.TM_CCOEFF_NORMED)

			#xác định vị trí
			min_val_ok, max_val_ok, min_loc_ok, max_loc_ok = cv2.minMaxLoc(result_ok)
			min_val_con, max_val_con, min_loc_con, max_loc_con = cv2.minMaxLoc(result_con)
			min_val_DLS22, max_val_DLS22, min_loc_DLS22, max_loc_DLS22 = cv2.minMaxLoc(result_DLS22)
			min_val_play, max_val_play, min_loc_play, max_loc_play = cv2.minMaxLoc(result_play)
			min_val_playing, max_val_playing, min_loc_playing, max_loc_playing = cv2.minMaxLoc(result_playing)
			min_val_read, max_val_read, min_loc_read, max_loc_read = cv2.minMaxLoc(result_read)
			min_val_x, max_val_x, min_loc_x, max_loc_x = cv2.minMaxLoc(result_x)
			min_val_xp, max_val_xp, min_loc_xp, max_loc_xp = cv2.minMaxLoc(result_xp)
			min_val_url, max_val_url, min_loc_url, max_loc_url = cv2.minMaxLoc(result_url)
			min_val_home, max_val_home, min_loc_home, max_loc_home = cv2.minMaxLoc(result_home)
			min_val_cancel, max_val_cancel, min_loc_cancel, max_loc_cancel = cv2.minMaxLoc(result_cancel)
			min_val_dls, max_val_dls, min_loc_dls, max_loc_dls = cv2.minMaxLoc(result_dls)
			min_val_mall, max_val_mall, min_loc_mall, max_loc_mall = cv2.minMaxLoc(result_mall)
			min_val_ch, max_val_ch, min_loc_ch, max_loc_ch = cv2.minMaxLoc(result_ch)
			min_val_fix, max_val_fix, min_loc_fix, max_loc_fix = cv2.minMaxLoc(result_fix)
			min_val_back, max_val_back, min_loc_back, max_loc_back = cv2.minMaxLoc(result_back)
			min_val_tw, max_val_tw, min_loc_tw, max_loc_tw = cv2.minMaxLoc(result_tw)
			min_val_twu, max_val_twu, min_loc_twu, max_loc_twu = cv2.minMaxLoc(result_twu)
			min_val_load, max_val_load, min_loc_load, max_loc_load = cv2.minMaxLoc(result_load)
			min_val_cc, max_val_cc, min_loc_cc, max_loc_cc = cv2.minMaxLoc(result_cc)
			min_val_cc1, max_val_cc1, min_loc_cc1, max_loc_cc1 = cv2.minMaxLoc(result_cc1)
			min_val_cc2, max_val_cc2, min_loc_cc2, max_loc_cc2 = cv2.minMaxLoc(result_cc2)
			min_val_cc3, max_val_cc3, min_loc_cc3, max_loc_cc3 = cv2.minMaxLoc(result_cc3)
			min_val_cc4, max_val_cc4, min_loc_cc4, max_loc_cc4 = cv2.minMaxLoc(result_cc4)
			min_val_cc5, max_val_cc5, min_loc_cc5, max_loc_cc5 = cv2.minMaxLoc(result_cc5)
			min_val_cc6, max_val_cc6, min_loc_cc6, max_loc_cc6 = cv2.minMaxLoc(result_cc6)
			min_val_cc7, max_val_cc7, min_loc_cc7, max_loc_cc7 = cv2.minMaxLoc(result_cc7)
			min_val_cc8, max_val_cc8, min_loc_cc8, max_loc_cc8 = cv2.minMaxLoc(result_cc9)
			min_val_cc9, max_val_cc9, min_loc_cc9, max_loc_cc9 = cv2.minMaxLoc(result_cc9)
			min_val_cc10, max_val_cc10, min_loc_cc10, max_loc_cc10 = cv2.minMaxLoc(result_cc10)
		except:
			continue
		if max_val_cc10 > 0.85:
			try:
				a, b = max_loc_cc10
				a +=32
				c = 140
				d = 30
				
				im = pg.screenshot(region=(a,b, c, d))
				im = cv2.cvtColor(np.array(im), cv2.COLOR_RGB2BGR)
				cv2.imwrite("Send.png", im)
				pytesseract.tesseract_cmd = "C:\\Program Files\\Tesseract-OCR\\tesseract.exe"
				time.sleep(1)
				img = cv2.imread("send.png")
				words = pytesseract.image_to_string(img)
				time.sleep(1)
				pg.click(max_loc_cc9)
				pg.write(words)
				time.sleep(1)
				pg.press('enter')
			except:
				pass
		if max_val_ok > 0.8:
			try:
				pg.click(max_loc_ok)
			except:
				pass
		if max_val_ch > 0.8:
			try:
				pg.click(max_loc_ch)
			except:
				pass
			time.sleep(2)
		if max_val_con > 0.8:
			try:
				pg.click(max_loc_con)
			except:
				pass
		if max_val_play > 0.8:
			try:
				pg.click(max_loc_play)
			except:
				pass
		if max_val_playing > 0.8:
			try:
				pg.click(max_loc_playing)
			except:
				pass
		if max_val_read > 0.8:
			try:
				pg.click(max_loc_read)
			except:
				pass
		if max_val_x > 0.8:
			try:    
				pg.click(max_loc_x)
			except:
				pass
		if max_val_xp > 0.8:
			try:
				pg.click(max_loc_xp)
			except:
				pass
		if max_val_url > 0.8:
			try:
				pg.click(max_loc_url)
				time.sleep(1)
				pg.write('DLS22 game')
				pg.press('enter')
			except:
				pass
		if max_val_home > 0.8:
			try:
				pg.click(max_loc_DLS22)
			except:
				pass
		if max_val_cancel > 0.8:
			try:
				pg.click(max_loc_cancel)
			except:
				pass
		if max_val_mall > 0.8: #1
			try:
				pg.click(max_loc_dls)
				time.sleep(200)
			except:
				pass
		if max_val_fix > 0.8: #2
			try:
				pg.click(max_loc_cc8)
			except:
				pass
		if max_val_tw > 0.8:
			try:
				pg.click(max_loc_tw)
			except:
				pass
		if max_val_twu > 0.8:
			try:
				pg.click(max_loc_twu)
				time.sleep(1)
				pg.write('DLS22 game')
				pg.press('enter')
			except:
				pass
		if max_val_cc > 0.8:
			try:
				pg.click(max_loc_cc)
			except:
				pass
		if max_val_cc1 > 0.8:
			try:
				pg.click(max_loc_cc1)
			except:
				pass
		if max_val_cc2 > 0.8:
			try:
				pg.click(max_loc_cc2)
			except:
				pass
		if max_val_cc3 > 0.8:
			try:
				pg.click(max_loc_cc3)
			except:
				pass
		if max_val_cc4 > 0.8:
			try:
				pg.click(max_loc_cc4)
			except:
				pass
		if max_val_cc5 > 0.8:
			try:
				pg.click(max_loc_cc5)
			except:
				pass
		if max_val_cc6 > 0.8:
			try:
				pg.click(max_loc_cc6)
				time.sleep(1)
				pg.click(max_loc_cc6)
				time.sleep(1)
				pg.click(max_loc_cc6)
				time.sleep(1)
				pg.click(max_loc_cc6)
			except:
				pass
		if max_val_cc7 > 0.8:
			try:
				pg.click(max_loc_cc7)
			except:
				pass
		#print("ok ", max_val_ok)..
		#print("con ", max_val_con)
		#print("DLS22 ", max_val_DLS22)
		#print("play ", max_val_play)
		#print("playing ", max_val_playing)
		#print("read ", max_val_read)
		#print("x ", max_val_x)
		#print("xp ", max_val_xp)
		#print("url ", max_val_url)
		#print("home ", max_val_home)
		#print("dls ", max_val_dls)
		#print("cancel ", max_val_cancel)
		#print("mall ", max_val_mall)
Screenshot_button = Button(button_frame, text="Chạy đi Bot occhoa", command=tool)
Screenshot_button.place(x=45, y=90)
root.mainloop()
