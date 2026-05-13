# Eventbrite Integration - May 13, 2026

## Summary
Updated XSL AI Academy website to link to live Eventbrite registration and display actual event details.

## Eventbrite Event
**URL:** https://www.eventbrite.com/e/work-smarter-with-claude-ai-realtor-edition-live-workshop-happy-hour-tickets-1989255236963?aff=oddtdtcreator

**Event Details:**
- **Date:** Wednesday, May 20, 2026
- **Time:** 3:00 PM - 5:00 PM (workshop) + 5:00 PM onward (happy hour)
- **Location:** Hyatt Regency Newport Beach, 1107 Jamboree Road, Newport Beach, CA 92660
- **Price:** $249
- **Includes:** 2-hour workshop, 2 drink tickets, materials

## Files Updated

### classes.html
✅ All "Register" buttons now link to Eventbrite
✅ Updated schedule from 2:00-4:00 PM → 3:00-5:00 PM
✅ Updated "Event Details" section with actual date/time/location
✅ Changed "one drink ticket" → "two drink tickets"

### index.html
✅ **Navigation CTA** - "Join Waitlist" → "Register Now" (Eventbrite link)
✅ **Mobile Menu CTA** - "Join the Waitlist" → "Register Now" (Eventbrite link)
✅ **Hero Section** - Updated CTA + location note with date/time/venue
✅ **Pricing Cards** - Both tiers now link to Eventbrite with clear pricing
✅ **Final CTA Section** - Replaced waitlist form with event details + Register button

## All Eventbrite Links Added (8 total)

1. Navigation bar (desktop)
2. Mobile menu
3. Hero section CTA
4. Classes page hero CTA
5. Pricing card - $249 tier
6. Pricing card - $299 tier
7. Classes page bottom CTA
8. Final CTA section (index.html)

## Design Changes

### Before
- "Join Waitlist" messaging
- Email collection form
- "Dates coming soon" messaging
- Generic "Coming to Orange County and San Diego"

### After
- "Register Now" with clear pricing
- Direct Eventbrite links (open in new tab)
- Actual date: Wednesday, May 20, 2026
- Specific time: 3:00-5:00 PM
- Venue: Hyatt Regency Newport Beach
- "2 drink tickets included" messaging

## Link Attributes
All Eventbrite links include:
- `target="_blank"` - Opens in new tab
- `rel="noopener"` - Security best practice for external links

## Next Steps
1. ✅ Test all links
2. Push to GitHub
3. Deploy to production
4. Test registration flow on live site
5. Monitor Eventbrite ticket sales

## Notes
- Kept both pricing tiers ($249 early bird, $299 standard) as shown on index.html
- Classes page shows $249 as the main price
- All buttons now clearly show "Register Now" instead of waitlist language
- Event is 7 days away (May 20 from May 13)
