from moviepy.editor import *

# مدة الفيديو بالثواني
duration = 5

# أنشئ خلفية لونها أزرق (ممكن تغير اللون)
clip = ColorClip(size=(640, 480), color=(0, 102, 204), duration=duration)

# ضيف النص
txt_clip = TextClip("أهلاً وسهلاً يا مينا\nكل سنة وأنت طيب", fontsize=50, color='white', font='Arial-Bold')
txt_clip = txt_clip.set_position('center').set_duration(duration)

# دمج النص مع الخلفية
video = CompositeVideoClip([clip, txt_clip])

# حفظ الفيديو
video.write_videofile("greeting_video.mp4", fps=24)
   

   
   
   


   
   
   


   
   
   



