# LearnSysDesign

## Design AirBnB

### Ask questions
#### Question 1
<b>Q: Like a lot of other sharing-economy products out there, Airbnb has two sides: a host-facing side and a renter-facing side. Are we designing both of these sides or just one of them?</b>
<br>A: Let's design both of these sides of the product.

#### Question 2
<b>Q: Okay. So we're probably designing the system for hosts to create and maybe delete listings, and the system for renters to browse through properties, book them, and manage their bookings afterwards. Is that correct?</b>
<br>A: Yes for hosts; but let's actually just focus on browsing through listings and booking them for renters. We can ignore everything that happens after booking on the renter-facing side.

#### Question 3
<b>Q: Okay, but for booking, is the idea that, when a user is browsing a property for a specific date range, the property gets temporarily reserved for them if they start the booking process?</b>
<br>A: Yes. More specifically, multiple users should be allowed to look at the same property, for the same date range, concurrently without issues. But once a user starts the booking process for a property, it should be reflected that this property is no longer available for the dates in question if another user tries to book it.

#### Question 4
<b>Q: I see. But so, let's say two users are looking at the exact same property for an overlapping date range, and one user presses "Book Now", at which point they have to enter credit card information. Should we immediately lock the property for the other user for some predetermined period of time, like maybe 15 minutes, and if the first person actually goes through with booking the property, then this "lock" becomes permanent?</b>
<br>A: Yes, that makes sense. In real life, there might be slight differences, but for the sake of this design, let's go with that.

#### Question 5
<b>Q: Okay. And do we want to design any auxiliary features like being able to contact hosts, authentication and payment services, etc., or are we really just focusing on browsing and reserving?</b>
<br>A: Let's really just focus on browsing and booking. We can ignore the rest.

#### Question 6
Q: I see. So, since it sounds like we're designing a pretty targeted part of the entire Airbnb service, I want to make sure that I know exactly every functionality that we want to support. My understanding is that users can go on the main Airbnb website or app, they can look up properties based on certain criteria, like location, available date range, pricing, property details, etc., and then they can decide to book a location. As for hosts, they can basically just create a listing and delete it like I said earlier. Is that correct?</b>
<br>A: Yes. But actually, for this design, let's purely filter based on location and available date range as far as listing characteristics are concerned; let's not worry about other criteria like pricing and property details.

#### Question 7
<b>Q: What is the scale that we're designing this for? Specifically, roughly how many listings and renters do we expect to cater to?</b>
<br>A: Let's only consider Airbnb's U.S. operations. So let's say 50 million users and 1 million listings.

#### Question 8
<b>Q: Regarding systems characteristics like availability and latency, I'm assuming that, even if a renter looks up properties in a densely-populated area like NYC, where there might be a lot of listings, we care about serving these listings fast, accurately, and reliably. Is that correct?</b>
<br>A: Yes, that's correct. Ideally, we don't want any downtime for renters browsing listings.
