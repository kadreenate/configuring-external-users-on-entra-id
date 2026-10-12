# configuring-external-users-on-entra-id
The purpose of this lab is to configure external user settings on Microsoft Entra ID

**Step 1: Enable guest users to perform self-service sign-ups**

On Microsoft Entra ID, select Users under Entra ID in the left navigation menu > go to User settings on the Users page. Under External users, select "Manage external user collaboration settings."

<img width="1177" height="830" alt="image" src="https://github.com/user-attachments/assets/cf623c08-f126-44cc-b7ba-18e872f031cc" />

Under Guest invite settings, toggle YES to **Enable guest self-service sign up via user flows.** > click **save** at the top

<img width="1050" height="660" alt="image" src="https://github.com/user-attachments/assets/ff8d9dd0-d454-40b8-8f4c-23303fe49084" />

**Step 2: Configure external collaboration settings**
In the left navigation menu, under Entra ID, select External Identities, and then select All identity providers. In the list of providers, select the Email one-time passcode item, then select Configured.

<img width="1201" height="741" alt="image" src="https://github.com/user-attachments/assets/cadadd93-180f-4859-a28d-2130f1a5b6ad" />

Ensure that Yes is selected. Select Save if needed: 

<img width="889" height="369" alt="image" src="https://github.com/user-attachments/assets/f9951126-c862-45b3-8563-2d1708bf44cc" />

On the External Identities menu, select External Collaboration Settings on the left. Under Guest user access, review the available access levels, then select **Guest user access is restricted to properties and memberships of their own directory objects (most restrictive).**

Note:

_a. Guest users have the same access as members (most inclusive): This option gives guests the same access to Microsoft Entra resources and directory data as member users.
b. Guest users have limited access to properties and memberships of directory objects (Default): This setting blocks guests from certain directory tasks, like enumerating users, groups, or other directory resources. Guests can see membership of all non-hidden groups.
c. Guest user access is restricted to properties and memberships of their own directory objects (most restrictive): With this setting, guests can access only their own profiles. Guests are not allowed to see other users' profiles, groups, or group memberships._

<img width="1227" height="687" alt="image" src="https://github.com/user-attachments/assets/67b6cc1b-bafb-4920-87f7-a91da3f36e16" />

Under Guest invite settings, select **Member users and users assigned to specific admin roles can invite guest users including guests with member permissions
**
Note: 

a. _Anyone in the organization can invite guest users including guests and non-admins (most inclusive): To allow guests in the organization to invite other guests including those who are not members of an organization, select this radio button.
b. Member users and users assigned to specific admin roles can invite guest users, including guests with member permissions: To allow member users and users who have specific administrator roles to invite guests, select this radio button.
c. Only users assigned to specific admin roles can invite guest users: To allow only those users with administrator roles to invite guests, select this radio button. The administrator roles include Global Administrator, User Administrator, and Guest Inviter.
d. No one in the organization can invite guest users, including admins (most restrictive): To deny everyone in the organization from inviting guests, select this radio button.
If Members can invite is set to No and Admins and users in the guest inviter role can invite is set to Yes, users in the Guest Inviter role will still be able to invite guests._

<img width="741" height="280" alt="image" src="https://github.com/user-attachments/assets/55ee6586-7b4d-4719-9965-841f783a88ad" />

Under Collaboration restrictions, review the available options and accept the default settings: 

<img width="730" height="345" alt="image" src="https://github.com/user-attachments/assets/9b42e35f-4910-40d6-82aa-42e8be8f6f79" />

Note:

a. You can create either an allow list or a deny list. You can't set up both types of lists. By default, whatever domains are not in the allow list are on the deny list, and vice versa.
b. You can create only one policy per organization. You can update the policy to include more domains, or you can delete the policy to create a new one.
c. The number of domains you can add to an allow list or deny list is limited only by the size of the policy. The maximum size of the entire policy is 25 KB (25,000 characters), which includes the allow list or deny list and any other parameters configured for other features.
d. This list works independently from OneDrive for Business and SharePoint Online allow/block lists. If you want to restrict individual file sharing in SharePoint Online, you need to set up an allow or deny list for OneDrive for Business and SharePoint Online.
e. The list does not apply to external users who have already redeemed the invitation. The list will be enforced after the list is set up. If a user invitation is in a pending state, and you set a policy that blocks their domain, the user's attempt to redeem the invitation will fail.

When finished, save your changes.

