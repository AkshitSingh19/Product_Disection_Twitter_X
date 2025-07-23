# **X (Twitter) Product Dissection Case Study**

<img width="800" height="300" alt="X_profile" src="https://github.com/user-attachments/assets/804b01f7-e846-4e2f-bd09-a3be32429d64" />

## **Overview**
This project presents a comprehensive **product dissection and schema design** for **X (formerly Twitter)** — one of the world’s most influential platforms for real-time information and public discourse. The goal is to analyze the platform's core features, explore its real-world impact, and model its data architecture through schema and ER diagram representation.

🔗 **GitHub Repository:** [X Product Dissection and Schema Design](https://github.com/AkshitSingh19/Product_Disection_Twitter_X))

---

## **Company Overview**
**Twitter**, now officially known as **X**, was launched in 2006 and has since evolved into a global social communication powerhouse. It allows users to broadcast messages (tweets), interact with global communities, follow trends, and participate in public discussions in real-time.

- Founded by Jack Dorsey, Noah Glass, Biz Stone, and Evan Williams.
- Rebranded as **X** in 2023 under Elon Musk’s leadership.
- Over **400 million users** globally.
- Known for brevity, speed, and influence in political, social, and cultural events.

---

## **Key Features of X (Twitter)**
1. **User Profiles** – Personalized identity with bios, usernames, and profile pictures.
2. **Tweets & Threads** – 280-character posts with support for media, hashtags, and threads.
3. **Retweets & Quote Tweets** – Enables users to share and build on each other’s content.
4. **Followers/Following** – Build personal networks and communities.
5. **Hashtags & Explore** – Discover trending topics and conversations.
6. **Likes, Comments & Bookmarks** – Engagement tools for interaction.
7. **Twitter Spaces** – Real-time audio conversations.
8. **Community Notes** – Fact-checking by the community to prevent misinformation.

---

## **Real-World Problems Solved by Twitter**

### 1. **Information Overload & Content Discovery**
- **Challenge:** Millions of tweets cause users to miss key updates.
- **Solution:** Trending Topics, Hashtags, and Topic Following for curated discovery.

### 2. **Short-Form Limitations**
- **Challenge:** 140/280 characters hinder in-depth expression.
- **Solution:** Tweet Threads, Quote Tweets, and extended character limits.

### 3. **Online Harassment & Safety**
- **Challenge:** Trolls, abuse, and toxic content.
- **Solution:** Mute/Block tools, Hide Replies, Mute Keywords, and reporting features.

### 4. **Misinformation**
- **Challenge:** Difficulty discerning facts from fake news.
- **Solution:** Verified Badges, Fact-Check Labels, and Community Notes.

---

## **Schema Design**

### **Entities and Attributes**

1. **User**
   - `UserID` (PK)
   - `Username`
   - `Email`
   - `Full_Name`
   - `Bio`
   - `Registration_Date`

2. **Tweet**
   - `TweetID` (PK)
   - `UserID` (FK)
   - `Caption`
   - `Image_URL`
   - `Location`
   - `Tweet_Date`

3. **Comment**
   - `CommentID` (PK)
   - `TweetID` (FK)
   - `UserID` (FK)
   - `Text`
   - `Comment_Date`

4. **Like**
   - `LikeID` (PK)
   - `TweetID` (FK)
   - `UserID` (FK)
   - `Like_Date`

5. **Follower**
   - `FollowerID` (PK)
   - `FollowingUserID` (FK)
   - `FollowerUserID` (FK)
   - `Follow_Date`

6. **Hashtag**
   - `HashtagID` (PK)
   - `Tag`

7. **TweetHashtag**
   - `TweetHashtagID` (PK)
   - `TweetID` (FK)
   - `HashtagID` (FK)

8. **Retweet**
   - `UserID` (PK)
   - `TweetID` (FK)
   - `Retweet_Date`
   - `Quote`
   - `Retweet_Pic`

---

## **Entity Relationships**

- Users **create** Tweets.
- Users **comment** on Tweets.
- Users **like** Tweets.
- Users **follow** each other.
- Users **retweet** Tweets.
- Tweets **use** Hashtags (many-to-many).
- Hashtags are **linked** to Tweets through the TweetHashtag entity.

---

## **ER Diagram**
📌 *Add ER Diagram Added in the repsitory*  
This diagram visually illustrates the relationships between the entities defined above.

---

## **Conclusion**
This case study explored how X (Twitter) tackles critical challenges in real-time digital communication and public interaction. From facilitating global conversations to addressing misinformation and online safety, X’s innovative features and schema design demonstrate its impact and scalability.

The schema model offers deep insights into how a microblogging platform is architected to support billions of interactions daily — ensuring responsiveness, clarity, and user safety in a high-volume social ecosystem.

---

## 📬 Contact
📩 **Email:** [asas.singh7@gmail.com](mailto:asas.singh7@gmail.com)  
🔗 **LinkedIn:** [linkedin.com/in/akshitsingh500](https://linkedin.com/in/akshitsingh500)  
🔗 **GitHub:** [github.com/AkshitSingh19](https://github.com/AkshitSingh19)

🚀 *Empowering communication, one tweet at a time.*  
⭐ *Star this repo if you found it useful!*
