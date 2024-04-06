# 密投(SecretVote)
不经意传输（Oblivious Transfer，OT）是一种密码学协议，它允许一个发送方（通常称为S）向接收方（通常称为R）发送信息，同时接收方可以选择接收其中的一部分信息，而发送方不会知道接收方选择了哪些信息。这个特性使得OT成为实现隐私保护投票系统的理想选择，因为它可以确保选民的投票隐私得到保护，同时投票的有效性也得到了保证。

在基于OT的隐私保护投票系统中，通常包含以下几个步骤：

初始化阶段：

发送方S持有两个或多个消息（例如，代表不同候选人的信息），并且每个消息都有一个与之关联的标识符。
接收方R拥有一个私有的投票选择（例如，选民想要投票给的候选人）。

OT协议执行：

通过执行OT协议，接收方R能够从发送方S那里获取与其投票选择相对应的消息，而发送方S无法得知接收方R选择了哪个消息。
这个过程确保了选民的投票选择不被泄露给任何第三方，包括发送方S。

投票收集与验证：

一旦所有选民都通过OT协议完成了投票，发送方S会收集所有未被接收的消息（即未被投票的消息）。
发送方S可以验证每个消息的完整性和正确性，但无法将消息与特定的选民关联起来。

结果统计：

发送方S根据收集到的投票信息统计投票结果。
由于发送方S不知道哪些消息被接收，因此无法推断出任何选民的投票倾向。

结果公布：

最后，发送方S公布投票结果，但不公布任何个体选民的投票信息。
通过这种方式，OT协议实现了一个关键的安全属性：接收方隐私（Receiver Privacy）。这意味着接收方R的选择对于发送方S是不可见的，从而确保了选民的隐私保护性。此外，由于发送方S无法得知哪些消息被接收，也无法从接收到的消息中推断出任何选民的投票选择，这进一步增强了系统的隐私保护能力。

在实际应用中，OT协议可以结合其他密码学技术，如同态加密、秘密分享等，来增强系统的安全性和隐私性。例如，可以使用同态加密来对投票结果进行加密计算，确保即使在统计过程中，投票信息也不会被泄露。

总之，OT协议为实现隐私保护投票系统提供了一种有效的技术手段，它通过确保选民的投票选择不被泄露，保护了选民的隐私权，同时也保证了投票过程的公正性和透明性。
