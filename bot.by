import os
from telegram import Update
from telegram.ext import Updater, CommandHandler, CallbackContext

# التوكن الخاص بالبـوت مباشرة أو من المتغير البيئي
TELEGRAM_TOKEN = '7296928281:AAGaM7lmAYiRsVnxW-I2w3czxb40orKtSQU'  # أو استخدام os.getenv('TELEGRAM_TOKEN') إذا كنت تستخدم المتغير البيئي

# دالة الرد على أمر "/start"
def start(update: Update, context: CallbackContext) -> None:
    update.message.reply_text('مرحبًا! كيف يمكنني مساعدتك؟')

# دالة رئيسية لتشغيل البوت
def main():
    # إنشاء Updater
    updater = Updater(TELEGRAM_TOKEN)

    # الحصول على dispatcher لإضافة المعالجات
    dispatcher = updater.dispatcher

    # إضافة معالج للأمر "/start"
    dispatcher.add_handler(CommandHandler("start", start))

    # بدء البوت
    updater.start_polling()

    # جعل البوت يعمل للأبد
    updater.idle()

if __name__ == '__main__':
    main()
