# Votelog
 vote on anything youw want and the app will pay the majority 


contract EtherVote {
    event LogVote(bytes32 indexed proposalHash, bool pro, address addr);
    function vote(bytes32 proposalHash, bool pro) {
        if (msg.value > 0) throw;
        LogVote(proposalHash, pro, msg.sender);
    }
    function () { throw; }
}

(a hash of the proposal being voted on,
if the voter agrees or disagrees with it,
the address of the voter)







