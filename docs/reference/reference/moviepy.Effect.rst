from moviepy.editor import *

# مدة الفيديو بالثواني
duration = 4

# خلفية لونها أخضر فاتح
clip = ColorClip(size=(640, 360), color=(102, 255, 102), duration=duration)

# النص الإنجليزي
txt_clip = TextClip("Hello, welcome!", fontsize=50, color='black', font='Arial-Bold')
txt_clip = txt_clip.set_position('center').set_duration(duration)

# دمج النص مع الخلفية
video = CompositeVideoClip([clip, txt_clip])

# حفظ الفيديو
video.write_videofile("light_english_video.mp4", fps=24)
   

   
   
   


   
   
   


   
   
   



