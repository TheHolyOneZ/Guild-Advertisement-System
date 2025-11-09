# Guild-Advertisement-System
The **Guild Advertisement System** is a professional cross-guild advertising platform that allows Discord servers to share advertisements with each other through a secure approval-based system. Server owners maintain complete control over who can advertise in their server, when ads are posted, and how frequently they appear.
> 💡 **Built for the Zygnal Ecosystem — to download and use this extension, you must be part of the Zygnal Ecosystem.**  
> This extension (cog) is part of the **Zygnal Ecosystem** and is only available through its supported platforms.  
> You can use it with:  
> - The **[Discord Bot Framework](https://github.com/TheHolyOneZ/discord-bot-framework)** — ideal for developers who want full control and flexibility *(includes an integrated extension marketplace)*, or  
> - The **[ZygnalBot](https://zygnalbot.de)** — a prebuilt, plug-and-play Discord bot *(also includes an integrated extension marketplace)*.  
>
> Browse and install extensions at [zygnalbot.com/extension](https://zygnalbot.com/extension).  
> For help or community discussions, join us on Discord: [discord.gg/sgZnXca5ts](https://discord.gg/sgZnXca5ts)
# 🎯 Guild Advertisement System Documentation

## 📋 Overview

The **Guild Advertisement System** is a professional cross-guild advertising platform that allows Discord servers to share advertisements with each other through a secure approval-based system. Server owners maintain complete control over who can advertise in their server, when ads are posted, and how frequently they appear.

---

## 🚀 Getting Started

### 📝 Available Commands

| Command | Aliases | Description |
|---------|---------|-------------|
| **Main Menu** | `!guildads` | `!gads`, `!ads` | Display the main advertisement system overview |
| **Request Permission** | `!guildads request <guild_id>` | `!gads req <guild_id>` | Request permission to advertise in another server |
| **Create Ad** | `!guildads create` | `!gads new`, `!gads add` | Create a new advertisement for your server |
| **List Ads** | `!guildads list` | `!gads ls`, `!gads show` | View all your server's advertisements |
| **Edit Ad** | `!guildads edit <ad_id>` | `!gads modify <ad_id>` | Modify an existing advertisement |
| **Toggle Ad** | `!guildads toggle <ad_id>` | `!gads enable/disable <ad_id>` | Enable or disable an advertisement |
| **Preview Ad** | `!guildads test <ad_id>` | `!gads preview <ad_id>` | Preview how your advertisement will look |
| **View Connections** | `!guildads connections` | `!gads conn`, `!gads links` | See all approved advertising connections |
| **Pending Requests** | `!guildads pending` | `!gads requests` | View incoming advertisement requests (owners only) |
| **Revoke Permission** | `!guildads revoke <guild_id>` | `!gads remove <guild_id>` | Remove advertising permission (owners only) |
| **View Statistics** | `!guildads stats` | `!gads statistics` | Display detailed advertising statistics |
| **Audit Log** | `!guildads audit` | `!gads log`, `!gads history` | View advertising activity history |
| **Manage Whitelist** | `!guildads whitelist` | `!gads wl` | Configure whitelist settings (owners only) |
| **Manage Blacklist** | `!guildads blacklist` | `!gads bl` | Configure blacklist settings (owners only) |
| **Cleanup Data** | `!guildads cleanup` | `!gads clean` | Remove invalid/old data (owners only) |

---

## 🎯 Core Features

### 📢 **For Advertisers**

#### 🚀 **Getting Started**
1. **Find Target Servers**: Identify servers where you want to advertise
2. **Request Permission**: Use `!guildads request <guild_id>` to ask for advertising rights
3. **Wait for Approval**: Server owners receive DM notifications with approval options
4. **Create Advertisements**: Once approved, create ads with `!guildads create`
5. **Monitor Performance**: Track ad delivery with statistics and audit logs

#### 📝 **Creating Advertisements**
- **Interactive Form**: User-friendly modal with guided input fields
- **Rich Embeds**: Create beautiful advertisements with titles, descriptions, and images
- **Dynamic Variables**: Use placeholders that auto-replace with server information
- **Color Customization**: Set custom embed colors with hex codes
- **Image Support**: Add banner images and thumbnails to advertisements

#### 🔄 **Dynamic Variables**
Make your ads personalized for each target server:
- `{server}` - Target server name
- `{origin_server}` - Your server name
- `{role}` - Mentioned role (if configured)
- `{member_count}` - Target server member count
- `{origin_member_count}` - Your server member count

### ⚙️ **For Server Owners**

#### 🔐 **Approval System**
- **DM Notifications**: Receive detailed requests directly in your DMs
- **Interactive Approval**: Use buttons and forms to approve/deny requests
- **Flexible Configuration**: Set channels, schedules, and limits during approval
- **Complete Control**: Approve, deny, or revoke permissions at any time

#### ⏰ **Scheduling Controls**
Configure exactly when ads can be posted:
- **Hour Restrictions**: `9-17` (business hours) or `9,12,15` (specific times)
- **Minute Controls**: `0,30` (half-hourly) or `*` (any minute)
- **Daily Limits**: Set maximum ads per day (1-20)
- **Flexible Timing**: Supports ranges, lists, or wildcards

#### 👥 **Role Integration**
- **Optional Mentions**: Allow role pings with advertisements
- **Role Selection**: Choose which role gets mentioned
- **Permission Control**: Decide if role mentions are allowed per connection

---

## 🛠️ How to Use

### 📤 **For Advertisers: Getting Permission**

#### 1️⃣ **Request Advertising Permission**
```
!guildads request 123456789012345678
```
- Replace the number with the target server's ID
- The server owner receives a detailed DM with your request
- Includes your server info, member count, and creation date

#### 2️⃣ **Create Your First Advertisement**
```
!guildads create
```
- Opens an interactive form with the following fields:
  - **Title**: Eye-catching headline for your ad
  - **Description**: Detailed information about your server
  - **Color**: Hex color code for embed styling
  - **Image**: Optional banner or thumbnail URL

#### 3️⃣ **Manage Your Advertisements**
```
!guildads list          # View all your ads
!guildads edit ad_1     # Edit a specific ad
!guildads toggle ad_1   # Enable/disable an ad
!guildads test ad_1     # Preview how it looks
```

### 📥 **For Server Owners: Managing Requests**

#### 1️⃣ **Receiving Requests**
- Requests arrive as DMs with detailed information
- Includes requester's server stats and member count
- Interactive buttons for approval or denial

#### 2️⃣ **Approving Requests**
When approving, configure:
- **Channel ID**: Where ads will be posted
- **Allowed Hours**: When ads can be sent (e.g., `9-21`)
- **Allowed Minutes**: Specific minutes (e.g., `0,30`)
- **Role Mentions**: Optional role to ping
- **Daily Limit**: Maximum ads per day

#### 3️⃣ **Managing Connections**
```
!guildads pending       # View pending requests
!guildads connections   # See all approved connections
!guildads revoke 12345  # Remove advertising permission
```

---

## 🔒 Security & Control Features

### 🛡️ **Whitelist System**
Control who can send requests to your server:

```
!guildads whitelist enable          # Enable whitelist mode
!guildads whitelist min_members 100 # Require minimum members
!guildads whitelist min_age 30      # Require minimum server age (days)
!guildads whitelist disable         # Disable whitelist
```

### 🚫 **Blacklist System**
Block specific servers from sending requests:

```
!guildads blacklist add 12345       # Block a specific server
!guildads blacklist remove 12345    # Unblock a server
!guildads blacklist clear           # Clear entire blacklist
!guildads blacklist                 # View current blacklist
```

### ⏱️ **Rate Limiting**
- **24-hour cooldown** between requests to the same server
- **Prevents spam** and excessive requests
- **Automatic cleanup** of old rate limit data

---

## 📊 Statistics & Monitoring

### 📈 **Advertisement Statistics**
Track your advertising performance:
- **Total Advertisements**: How many ads you've created
- **Active/Inactive**: Status breakdown of your ads
- **Outgoing Connections**: Servers where you can advertise
- **Daily Activity**: Ads sent and received today
- **Efficiency Metrics**: Success rates and delivery stats

### 📋 **Audit Logging**
Complete activity tracking:
- **Ad Delivery**: When and where ads were sent
- **Permission Changes**: Approvals, denials, and revocations
- **System Events**: Cleanup operations and configuration changes
- **User Actions**: Who performed what actions and when

### 🔍 **Connection Overview**
Monitor all advertising relationships:
- **Incoming**: Servers that advertise to you
- **Outgoing**: Servers where you advertise
- **Channel Information**: Where ads are posted
- **Schedule Details**: When ads are allowed
- **Usage Statistics**: Daily limits and current usage

---

## 💡 Advanced Features

### 🎨 **Advertisement Customization**
- **Rich Embeds**: Professional-looking advertisements
- **Custom Colors**: Match your server's branding
- **Image Integration**: Banners, logos, and thumbnails
- **Variable Replacement**: Dynamic content for each server

### ⚡ **Automated Scheduling**
- **Smart Timing**: Respects server-specific time restrictions
- **Daily Limits**: Automatic quota management
- **Random Selection**: Rotates through multiple ads
- **Timezone Aware**: Works across different time zones

### 🧹 **Data Management**
- **Automatic Cleanup**: Removes invalid connections and old data
- **Cache System**: Efficient server information storage
- **Audit Retention**: Configurable log retention periods
- **Performance Optimization**: Regular maintenance operations

---

## 🆘 Troubleshooting

### ❌ **Common Issues**

**"Guild not found or bot is not in that guild"**
- The bot must be in both servers for advertising to work
- Verify the guild ID is correct

**"You must wait X hours before making another request"**
- Rate limiting is active - wait for the cooldown period
- Each server pair has a 24-hour cooldown

**"Your guild has been blacklisted"**
- The target server has blocked your server from advertising
- Contact the server owner to discuss removal

**"Your guild does not meet whitelist requirements"**
- The target server has specific requirements (member count, age, etc.)
- Check requirements with server owner

### 🔧 **Permission Requirements**
- **Advertisers**: Administrator or Manage Server permissions
- **Server Owners**: Only server owners can approve requests and manage settings
- **Bot Permissions**: Send Messages, Embed Links, Use External Emojis

---

## 📈 Best Practices

### 🎯 **For Effective Advertising**
- **Clear Titles**: Make your server's purpose obvious
- **Engaging Descriptions**: Highlight unique features and benefits
- **Professional Images**: Use high-quality banners and logos
- **Respectful Requests**: Only request permission from relevant servers

### 🛡️ **For Server Security**
- **Review Requests Carefully**: Check server quality before approving
- **Set Appropriate Limits**: Don't overwhelm your channels with ads
- **Use Whitelist/Blacklist**: Control who can send requests
- **Monitor Activity**: Regular check audit logs and statistics

### ⚙️ **For Optimal Performance**
- **Regular Cleanup**: Use cleanup command monthly
- **Update Advertisements**: Keep content fresh and relevant
- **Monitor Statistics**: Track performance and adjust strategies
- **Maintain Connections**: Remove inactive or problematic connections

---

## 🌟 Example Workflows

### 📤 **Advertiser Workflow**
1. Find target server ID
2. `!guildads request 123456789`
3. Wait for approval notification
4. `!guildads create` to make first ad
5. `!guildads stats` to monitor performance

### 📥 **Server Owner Workflow**
1. Receive request DM
2. Review server information
3. Click "Approve" and configure settings
4. `!guildads connections` to monitor
5. `!guildads audit` to review activity

---

*This documentation covers all features of the Guild Advertisement System. The system provides a professional, secure way for Discord communities to cross-promote while maintaining complete control over their advertising environment.*
