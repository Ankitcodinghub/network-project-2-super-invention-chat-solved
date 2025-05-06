# network-project-2-super-invention-chat-solved
**TO GET THIS SOLUTION VISIT:** [Network Project 2-Super Invention Chat Solved](https://www.ankitcodinghub.com/product/network-project-2-super-invention-chat-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;96224&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;Network Project 2-Super Invention Chat Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
Project: (UDP chat server and client)

In this exercise you will develop a chat server and the corresponding client application using UDP as transport layer protocol.

Protocol Format

All protocol fields are sent in network byte order. The Version field of client and server shall match. If they do not match the receiver may discard the packet and send a NAK. The Message Type can contain the following values:

• 0x01 – LOGIN

• 0x02 – MESSAGE • 0x03 – ACK

• 0x04 – NAK

• 0x05 – LOGOUT

The Message ID of a response must be identical to the Message ID of the corresponding request. Requests may pick a random number for the Message ID. The field Payload Length specifies the entire size of the following Payload. The content of Payload depends on the used Message Type:

LOGIN and LOGOUT: The payload contains a string to identify the client as CLIENT_ID. MESSAGE: The payload may contain up to two strings where the first one contains the

receiver CLIENT_ID and the second optionally contains the message to be sent. ACK and NAK: The payload must be empty.

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
Each string is represented by its Length and Content:

</div>
</div>
<div class="layoutArea">
<div class="column">
Protocol Flow

Messages of type LOGIN and LOGOUT must not be accepted by a client. Messages of type ACK and NAK must be discarded if no corresponding request using the same MESSAGE ID has been sent before. All messages of type LOGIN, LOGOUT, and MESSAGE must be answered with a message of type ACK or NAK. All erroneous are answered with a message of type NAK, all valid messages return an ACK message. If a server receives a message of type MESSAGE which contains two strings, it must store the content of the messages.

If a server receives a message of type MESSAGE which contains only one string, it must check whether a message for the requesting client has been stored and send this message back to the requesting client as message type MESSAGE. Messages may be delivered in a reversed order. The server must discard all messages of type MESSAGE if the given CLIENT_ID is not currently logged in (i.e., send a message of type LOGIN before, after the last LOGOUT message). The server may remove existing messages for the given CLIENT_ID upon reception of a LOGOUT message. A client must discard any unsolicited message of type MESSAGE.

1. Implement a server application which is expects the UDP port to listen on as command line parameter, e.g., ./udpchatserver &lt;PORT&gt;.

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
2. Implement a client application which expects three command line parameters: the address of the server, the port of the server, and a command. The command can be either login, logout, send, or receive.

• If the client application gets called with login or logout it shall request the CLIENT ID from the user via stdin.

• If the client application gets called with send it shall request the CLIENT ID from the user via stdin first and the message itself next.

• If the client application gets called with receive it shall send the message to server immediately.

</div>
</div>
</div>
