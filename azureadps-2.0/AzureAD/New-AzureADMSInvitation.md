---
external help file: Microsoft.Open.MS.GraphV10.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# New-AzureADMSInvitation

## SYNOPSIS
This cmdlet is used to invite a new external user to your directory.

## SYNTAX

```
New-AzureADMSInvitation [-InvitedUserDisplayName <String>] -InvitedUserEmailAddress <String>
 [-SendInvitationMessage <Boolean>] -InviteRedirectUrl <String>
 [-InvitedUserMessageInfo <InvitedUserMessageInfo>] [-InvitedUserType <String>] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet is used to invite a new external user to your directory.

## EXAMPLES

### Invite a new external user to your directory
```
New-AzureADMSInvitation -InvitedUserEmailAddress someexternaluser@externaldomain.com -SendInvitationMessage $True -InviteRedirectUrl "http://myapps.microsoft.com"

Id                      : 6058156a-93d1-4958-a738-ddc4ab4432cf
InvitedUserDisplayName  :
InvitedUserEmailAddress : someexternaluser@externaldomain.com
SendInvitationMessage   : True
InviteRedeemUrl         : https://login.microsoftonline.com/redeem?rd=https%3a%2f%2finvitations.microsoft.com%2fredeem%2f%3ftenant%3d06f6521d-c18c-460a-8656-fa82e81aa94b%26user%3d7b67d069-163b-4f7e-9118-c9ceeda363d9%26ticket%3ddANXuWQMNhYv21%252bFBm%252fULkTqCnpX6vNvRgTHQmsECPU%253d%26ver%3d2.0
InviteRedirectUrl       : http://myapps.microsoft.com/
InvitedUser             : class User {
                            Id: 04fd8318-77ca-428e-b7f2-2bb1ef7a0100
                            OdataType:
                          }

InvitedUserMessageInfo  : class InvitedUserMessageInfo {
                            CcRecipients: System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.Recipient]
                            CustomizedMessageBody:
                            MessageLanguage:
                          }

InvitedUserType         : Guest
Status                  : PendingAcceptance
```

Using the cmdlet in this example, an email is sent to the user whose email address is in the -InvitedUserEmailAddress parameter.
When the user accepts the invitation, they are forwarded to the url as specified in the -InviteRedirectUrl parameter

## PARAMETERS

### -InvitedUserDisplayName
The display name of the user as it will appear in your directory.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InvitedUserEmailAddress
The Email address to which the invitation is sent.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InvitedUserMessageInfo
Additional information to specify how the invitation message is sent

```yaml
Type: InvitedUserMessageInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InvitedUserType
The userType of the user being invited.
By default, this is Guest.
You can invite as Member if you're are company administrator.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InviteRedirectUrl
The URL to which the invited user is forwarded after accepting the invitation.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SendInvitationMessage
A Boolean parameter that indicates whether or not an invitation message will be sent to the invited user.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
