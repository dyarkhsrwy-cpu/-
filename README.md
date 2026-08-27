from rubka import Robot

TOKEN = "BCHHHA0DMHTULTRUUVIDWAKSFDMEFDCVPSUZVPYOELTKNXLTTFQZEIXDJMXVDGCP"

bot = Robot(TOKEN)

@bot.on_message()
async def handle_message(message):
    text = getattr(message, "text", "") or ""

    if text == "/start":
        await message.reply("✅ ربات روبیکا فعال است!")
    elif text == "/test":
        await message.reply("🟢 تست موفق بود؛ ربات در حال کار است.")

bot.run()
