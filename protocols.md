# Controllers

<table>
    <tr>
        <th>Protocol</th>
        <th>Connector</th>
        <th>Voltage</th>
    </tr>
{% for protocol in site.protocols %}
    <tr>
        <td><a href="{{ protocol.url }}">{{ protocol.name }}</a></td>
        {% assign connector = site.connectors[protocol.connector] %}
        <td><a href="{{ connector.url }}">{{ connector.name }}</td>
        <td>{{ protocol.voltage }}</td>
    </tr>
{% endfor %}
</table>