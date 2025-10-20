from telegram.ext import ApplicationBuilder, CommandHandler, MessageHandler, filters#birinchi
Token = "8000645038:AAF9hd9UaJNFNvi4JYwqDSJaScANJTa9YUI"#ikkinchi
async def start(update, context):
    await update.message.reply_text(
    "Assalamu alaykum🙂\n"
    "Sizga qanday yordam kerak"#uchinchi
    )
async def about(update, context):
    await update.message.reply_text(
    "Bu bot haqida ma'lumot qiziq ekan\n"
    "Unda bu ma'lumot siz uchun"
    "Siz bilgan bu botning\n"
    "Muallifi:Zubayr"
    "Botning yasalgan sana: 19.10.2025\n"
    "Ishga tushgan vaqti:20.10.2025\n"
    )
async def help(update, context):
       await update.message.reply_text(
       "Qanday muammo bor?\n"
       "Bu muammo oddiy "
       "Shu bot ichida eplasa bo'ladi"
       "/start - Asosiy menuga qaytish"
       "/about - Bot ma'lumotlarini bilish"
       "Juda kotta muammo"
       "Adminga bog'lanishim shart"
       "/admin - Adminga Bog'lanish"
       "Bu admin bilan bog'lanish uchun"
       )
async def admin(update, context):
    await update.message.reply_text(
       "Admin:n_z984"
       "Bu admin bilan bog'lanish uchun"
       )
def main():
    app = ApplicationBuilder().token(Token).build()
    app.add.handler(CommandHandler("start", start))
    app.add.handler(CommandHandler("about", about))
    app.add.handler(CommandHandler("help", help))
    app.add.handle(CommandHandler("admin", admin))
    print("🟢Bot ishga tushdi")
    app.run.polling()
    
if name == "main":
    main()
