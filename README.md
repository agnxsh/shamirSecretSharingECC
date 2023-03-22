<h1>Shamir Secret Sharing Algorithm using Elliptic Curve Cryptography</h1>
<p>
With secret sharing we take a secret value and then share it with others. For example we might have a share for Bob, Alice, Carol and Dave and then for three of them to come together to bring their shares together. For this we define a threshold (t) and a number of shares (n). We reconstruct the shares we need at least t shares to come together to reveal the secret. If we have (t-1) shares it should be impossible to reconstruct the secret.

For an any 3-from-4, we can use a quadratic equation, such as f(x)=20x2−2x+10
, and where the value of 10 is the secret. Bob then gets the value of f(x)
when x=0
 - and which is defined as f(1)
. Carol gets f(2)
, Dave gets f(3)
and Alice gets f(4)
. The secret value is thus f(0)
. They then each know a y-co-ordinate point on the quadratic equation. When they want to bring the value back, we can curve fit the gathered points. Thus if we have f(1)
, f(2)
and f(3)
we can regenerate the quadratic equation and thus determine f(0)
. We, of course, need to remember the x co-ordinate values for each share, so we give each share an ID of 1, 2, 3, and so on. Here we have three sample shares from an any 2-from-3 share, and notice that we have the x-co-ordinate value, so that when we reconstruct, we know the x
-co-ordinate for the share:</p>
