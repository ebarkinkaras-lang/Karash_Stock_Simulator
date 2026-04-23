KARASH Trading Simulator HTML entegrasyonu

1) İndikatör alanlarını serbest metin yerine sadece iki seçenekli select yap:
   - MC-Predict HullMA
   - MACD DEMA Pro

2) Kullanıcı en fazla iki indikatör seçsin. Aynı ikisi birlikte seçilirse bot ortalama skor kullanır.

3) Slot JSON yapısı:
{
  "id": "slot-1",
  "name": "Benim Simülasyonum",
  "exchange": "NASDAQ",
  "capital": 10000,
  "indicators": ["MC-Predict HullMA", "MACD DEMA Pro"],
  "active": true,
  "stopped": false,
  "cash": 10000,
  "portfolio_value": 10000,
  "pnl_pct": 0,
  "open_positions": [],
  "trade_log": []
}

4) Ana ekranda her kartta göster:
   - slot.name
   - slot.exchange
   - slot.indicators.join(' + ')
   - slot.pnl_pct
   - slot.portfolio_value + slot.currency
   - slot.last_run

5) Detay ekranında trade_log dizisini tabloya bas:
   - date
   - action
   - ticker
   - qty
   - price
   - score
   - cash_after
   - reason

6) HTML tarafında slot sayısı sabit olmasın. + Yeni Simülasyon ile sınırsız slot eklenebilsin.
