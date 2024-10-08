# **Filter HTTP Traffic**
Wireshark offers two types of filters: **Capture Filters** to capture the selected traffic, and **Display Filters** to analyze the captured traffic.

## Capture Filters
Prior to capturing the packets, assign a filter to the selected interface using the following options:

- The **Capture filter** field in the welcome screen

![capture filter field](../media/5-capture-filters.jpg)

- The **Capture** menu on the main toolbar

![capture menu](../media/6-capture-options.jpg)

1. Select **Capture > Capture Options**.
2. In the filter line, enter the necessary filter. It will be assigned to the selected interface.

The available filters show in the **Capture filters** section. Here, you can add and remove them.

![list of filters](../media/7-add-remove-filters.jpg)

## Display Filters
**Display filters** apply after you stop capturing the traffic. The most commonly used filtering options are as follows:

- Enter `HTTP` to display only the packets using the HTTP protocol.
![filtering option 1](../media/8-display-filters-case1.jpg)

- Enter the protocol and port filter to display all the HTTP traffic, including handshake and termination TCP packets.
![filtering option 2](../media/9-display-filters-case2.jpg)

- Use `and` / `or` operators to make filters with multiple parameters. For example, if you need to filter the HTTP traffic exchanged with a specific IP address, enter the two parameters into the display filter line.
![filtering option 3](../media/10-display-filters-case3.jpg)

- Use `http.request.method` filter type to filter specific HTTP packets (GET, PUT, POST, DELETE, HEAD, CONNECT, TRACE, etc.). For example, to filter only GET requests, enter this filter into the display filter line.
![filtering option 4](../media/11-display-filters-case4.jpg)

To trace the full HTTP stream, right-click on the HTTP packet and choose **Follow > HTTP Stream**. You will see a window with the full stream: request (in red) and response (in blue).

![full HTTP stream](../media/12-stream-outcome.jpg)
