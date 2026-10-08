# Hotel Booking Demand: Why Do Guests Cancel?

An analysis of 119,390 bookings from two Portuguese hotels (a City Hotel and a Resort Hotel), July 2015 – August 2017.

## Project layout

```
hotel_bookings/
├── README.md                        this file
├── requirements.txt                 Python packages the notebook needs
├── hotel_bookings_analysis.ipynb    the full analysis, every step explained
├── data/
│   └── hotel_bookings.csv           raw data (one row per booking, 32 columns)
└── figures/                         the 8 charts from the notebook, as PNG
```

## Key findings

1. **37% of bookings are cancelled**, worth EUR 16.7M of room value (39% of everything booked). City Hotel 42%, Resort Hotel 28%.
2. **Lead time is the strongest everyday driver**: 10% of bookings made within a week are cancelled, versus 68% of bookings made over a year ahead.
3. **About 14,600 "non-refundable" bookings are cancelled 99% of the time.** They behave like agency block bookings, not individual guests, and account for a third of all cancellations. They also explain most of Portugal's high cancellation rate.
4. **Committed guests rarely cancel**: special requests (17–22% vs 48%), repeat guests (15% vs 38%), direct bookings (15% vs 37% for online agents).
5. **"August is busiest" is a counting artefact**: July and August appear in 3 years of data, other months in 2. In 2016 the City Hotel peaks in spring and autumn. The Resort earns most in summer because of price and length of stay.
6. **A model using only booking-time information predicts cancellations with AUC 0.83** on 2017 data.

## How to run

1. Install the packages: `pip install -r requirements.txt`
2. Open `hotel_bookings_analysis.ipynb` in VS Code or Jupyter **from this folder** (the notebook reads `data/hotel_bookings.csv` and writes charts to `figures/`).
3. Choose *Run All*.

The notebook is saved with all outputs, so you can also just read it without running it.

## Data source

Hotel booking demand dataset by Nuno Antonio, Ana de Almeida and Luis Nunes: "Hotel booking demand datasets", *Data in Brief* 22 (2019) 41–49. https://doi.org/10.1016/j.dib.2018.11.126
