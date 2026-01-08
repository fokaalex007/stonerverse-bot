import asyncio
from aiogram import Bot, Dispatcher
from aiogram.types import (
    Message,
    InlineKeyboardMarkup,
    InlineKeyboardButton
)
from aiogram.filters import Command

BOT_TOKEN = "8520755539:AAETOp3_n-6vM9XDDl7JREfQftJCtYdjBPI"

WHATSAPP_NUMBER = "https://wa.me/qr/WZCUKZ7ANGHJN1"
POTATO_LINK = "https://m.dympt.org/stonerverse"
MINI_APP_URL = "https://example.com"  # placeholder for now


bot = Bot(token=BOT_TOKEN)
dp = Dispatcher()


@dp.message(Command("start"))
async def start(message: Message):
    keyboard = InlineKeyboardMarkup(inline_keyboard=[
        [
            InlineKeyboardButton(text="💬 WhatsApp", url=WHATSAPP_NUMBER),
            InlineKeyboardButton(text="🥔 Potato", url=POTATO_LINK)
        ],
        [
            InlineKeyboardButton(text="📱 Mini App", url=MINI_APP_URL)
        ]
    ])

    await message.answer(
        "👋 **Welcome to Stonerverse**\n\n"
        "Browse our catalog using the Mini App or contact us directly.",
        reply_markup=keyboard,
        parse_mode="Markdown"
    )


async def main():
    await dp.start_polling(bot)


if __name__ == "__main__":
    asyncio.run(main())
