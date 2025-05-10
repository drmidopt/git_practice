
from telegram import Update
from telegram.ext import Updater, CommandHandler

def start(update: Update, context):
    update.message.reply_text("مرحبًا! أنا بوت إدارة مشروع العلاج الطبيعي. استخدم:\n/upload - لرفع ملف\n/plan - لعرض الخطة العلاجية")

def upload(update: Update, context):
    update.message.reply_text("أرسل الملف الآن وسأحفظه في القناة.")

# استبدال 'TOKEN' بالرقم الذي أرسلته
updater = Updater("7789242899:AAHH-pK1drN_Wxv5wIpBv24aIIXgWsaF68Y", use_context=True)
updater.dispatcher.add_handler(CommandHandler('start', start))
updater.dispatcher.add_handler(CommandHandler('upload', upload))
updater.start_polling()
